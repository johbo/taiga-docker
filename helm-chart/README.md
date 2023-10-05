# Taiga 6 Helm chart


## Known limitations

Is mandatory to deploy taiga as taiga as chart name becase some names (related
to rabbitmq, take a look to `settings/config.py`) cannot be parametrized in
docker images.


## Volume handling

The chart does by default deploy two `PersistentVolumeClaim` (PVC) resources:

- `tagia-media` - This holds the media files. These files are content of the
  users, comparable to the content of the database.

- `taiga-static` - This holds static files which are filled by utility
  `collectstatic` of the Django framework.
