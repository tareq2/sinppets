## Automapper Version 6

    Mapper.Initialize(cfg => {
        cfg.CreateMap<Table1, Table2DTO>();

        cfg.CreateMap<Table2, Table2DTO>();
    });


## Manual Mapping Fields
To make the following mapping
PatientID ==> Id
Job==> Company
We use
AutoMapper.Mapper.CreateMap<User, Patient>().ForMember(dest => dest.PatientID, opt => opt.MapFrom(src => src.ID))  
  
               .ForMember(dest => dest.Job, opt => opt.MapFrom(src => src.Company)  
  
               ); 

## With Condition 

You can also map your objects based upon the condition. Let’s say we have the same two classes User and UserEntity and I have mapped the UserName to UserDetails only if it Contains Kovai.Co. So it can be done as,

     CreateMap<User, UserEntity>()
    .ForMember(d => d.Id, op => op.MapFrom(ex => ex.UserId))
    .ForMember(d => d.UserDetails, op => op.Condition(src => src.UserName.Contains("Kovai.Co")));
    
 ## Null Substitution
     CreateMap<Source, Dest>()
    .ForMember(destination => destination.Value, opt => opt.NullSubstitute("Any other values")));
