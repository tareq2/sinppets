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
