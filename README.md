# desafio-bsale-back

## Framework y librerΓ­as usadas

* Framework [Nestjs](https://nestjs.com/)
* ORM [TypeORM](https://typeorm.io/)

## Deploy

El despliegue del api rest se hizo en [Heroku](https://www.heroku.com/)
> Nota: Los accesos directos al api rest se encuentran en el apartado **Endpoints** π

## Estructura de carpetas

```text
src
βββ routes
β   βββ category
β   β   βββ category.controller.ts
β   β   βββ category.module.ts
β   β   βββ category.service.ts
β   β   βββ category.ts
β   βββ product
β       βββ product.controller.ts
β       βββ product.module.ts
β       βββ product.service.ts
β       βββ product.ts
βββ app.controller.ts
βββ app.module.ts
βββ app.service.ts
βββ main.ts
```

## Endpoints

| Route | Type | Input | Query |
| - | - | - | - |
| [/category/all](https://desafio-bsale-back.herokuapp.com/category/all) | `GET` | void | SELECT * FROM category; |
| [/product/all](https://desafio-bsale-back.herokuapp.com/product/all) | `GET` | void | SELECT * FROM product; |
| [/product/name/:name](https://desafio-bsale-back.herokuapp.com/product/name/ron) | `GET` | name: string | SELECT * FROM product WHERE name LIKE '%name%'; |
| [/product/category/:idCategory](https://desafio-bsale-back.herokuapp.com/product/category/1) | `GET` | idCategory: number | SELECT * FROM product WHERE category = 'idCategory' |