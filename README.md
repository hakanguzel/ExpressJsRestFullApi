
**ExpressJs RestFull Api**

Bu restfull servisinde kullanılan teknolojiler Nodejs, Express ve MySQL


MySQL konfigürasyon

    CREATE DATABASE expressjsrestfullapi;
    
    CREATE  TABLE IF NOT EXISTS `employees` (
      `id` BIGINT UNSIGNED AUTO_INCREMENT,
      `first_name` VARCHAR(255) NOT NULL,
      `last_name` VARCHAR(255) NOT NULL,
      `email` VARCHAR(255) NOT NULL,
      `phone` VARCHAR(50) NOT NULL,
      `organization` VARCHAR(255) NOT NULL,
      `designation` VARCHAR(100) NOT NULL,
      `salary` DECIMAL(11,2) UNSIGNED DEFAULT 0.00,
      `status` TINYINT UNSIGNED DEFAULT 0,
      `is_deleted` TINYINT UNSIGNED DEFAULT 0,
      `created_at` DATETIME NOT NULL,
      `updated_at` DATETIME DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
      PRIMARY KEY (`id`))
    ENGINE = InnoDB;
    INSERT INTO `expressjsrestfullapi`.`employees` (`first_name`, `last_name`, `email`, `phone`, `organization`, `designation`, `salary`, `status`, `is_deleted`, `created_at`) VALUES ('John', 'Doe', 'johndoe@gmail.com', '1234567890', 'HG Softech Ltd', 'Full Stack Developer', '500.00', '1', '0', '2020-06-14 12:50:30');
    INSERT INTO `expressjsrestfullapi`.`employees` (`first_name`, `last_name`, `email`, `phone`, `organization`, `designation`, `salary`, `status`, `is_deleted`, `created_at`) VALUES ('Jane', 'Doe', 'janedoe@gmail.com', '9876543210', 'HG Softech Ltd', 'PHP Developer', '450.00', '1', '0', '2020-06-14 12:50:30');

Lütfen veritabanını oluşturun ve `config/db.config.js` dosyasını düzeltin.

Projeyi çalıştırmak için proje klasöründe

    npm install

`node server.js` veya `nodemon start` veya `npm start`


`http://localhost:5000` adresini tarayıcınızda açınız.
