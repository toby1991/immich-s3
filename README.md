# Immich S3

Immich server with rclone, along with s3, webdav, etc...

## Usage
1. Change the `minio` config for yours in the `rclone/rclone.conf`
  * access_key_id: `YOUR_BUCKET_ACCESS_ID`
  * secret_access_key: `YOUR_BUCKET_ACCESS_KEY`
  * endpoint: `https://your-minio.yours.com`
2. Change the `.env` file for Immich Instance's DB config
  * IMMICH_DB_PASSWORD: `your_immich_db_password`
  * IMMICH_DB_USERNAME: `your_immich_db_username`
  * IMMICH_DB_DATABASE_NAME: `immich`
3. Change the `docker-compose.yaml` file for your own `minio` bucket
  * YOUR_BUCKET_NAME: `YOUR_BUCKET_NAME`
4. Run it
```bash
docker-compose up
```
5. Then you could access the **Immich Instance** at **[http://127.0.0.1](127.0.0.1)**
6. After configured your Immich, Add the external libraries via **[http://127.0.0.1/admin/library-management](http://127.0.0.1/admin/library-management)**, Add path `/usr/src/app/external/YOUR_BUCKET_NAME` to your Immich, then **Scan** it!
