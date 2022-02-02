Django Swagger 
---
This project is to show how to add beautiful Swagger documentation to your Django REST API.

## Steps
* Create a sample Django, DRF project using `django-admin`
* Install the `drf-spectacular` packacge
```bash
pip install drf-spectacular
```
* Add it to `INSTALLED_APPS` section in the `settings.py` file
* Also register `AutoSchema` with DRF in the `REST_FRAMEWORK` section as follows:
```bash
REST_FRAMEWORK = {
	...
    "DEFAULT_SCHEMA_CLASS": "drf_spectacular.openapi.AutoSchema",
}
```
* Now update the `urls.py` section, which basically imports `SpectacularAPIView` and `SpectacularSwaggerView`. Please refer to the `config/urls.py` file.
* Not create a `templates/swagger-ui.html` file and populate it.
* That's it : Visit [http://127.0.0.1:8000/docs/](http://127.0.0.1:8000/docs/)


### Screenshot
![Django Swagger UI screenshot](https://github.com/chef-platterbay/django-swagger/blob/master/Django_Swagger_UI_screenshot.png "Django Swagger UI screenshot")


#### Reference
* [Reference Blog](https://hackernoon.com/openapi-30-schema-with-swagger-ui-for-django-restful-app-4w293zje)
