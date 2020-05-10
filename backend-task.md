---------
1- Get seller offers listing
---------
- Description:
    - should return offers listing for the logged in seller (use seller id as param to avoid the need to implementing auth module).

- URL: `{{url}}/offers?page=1&per_page=10&sort[price]=asc&filter[status]=live`
- Type: `GET`
- Headers: `Token`
- Request Params: `page, per_page, seller_id=id, 
- Response Schema:
```
{
    data: {
      offers: [
        {
            id,
            title,
            image,
            price,
            last_updated,
        },
        {
            id,
            title,
            image,
            price,
            last_updated,
        },
      ],
      paging: {
        total: 20,
        current_page: 1,
        per_page: 10
      }
    }
}
```
- Entities: `Seller, Offer`
- Please use clean architecture to impelement this endpoint.
- Please use TypeScript, Mysql, TypeORM and Express to impelement this endpoint.
- Please use a caching mechanism (for ex Redis) to cache the data requested to be fetched from DB once and then from cache.
- Please add unit tests to the code you will write using any testing framework (jest is preferred).
- Please use small git commits (Not just one Large [initial commit]).
- Please generate swagger documentation for this API endpoint.
- Please put this on a public git Repo with steps to run in a `README` file.
