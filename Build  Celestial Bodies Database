postgres=> CREATE DATABASE universe;
CREATE DATABASE
postgres=> \c universe;
SSL connection (protocol: TLSv1.3, cipher: TLS_AES_256_GCM_SHA384, bits: 256, compression: off)
You are now connected to database "universe" as user "freecodecamp".
universe=> CREATE TABLE galaxy (
universe(>     galaxy_id SERIAL PRIMARY KEY,
universe(>     name VARCHAR NOT NULL UNIQUE,
universe(>     description TEXT,
universe(>     num_stars INT NOT NULL,
universe(>     num_planets INT NOT NULL,
universe(>     has_black_hole BOOLEAN
universe(> );
CREATE TABLE
universe=> INSERT INTO galaxy (name, description, num_stars, num_planets, has_black_hole)
universe-> VALUES
universe->     ('Milky Way', 'The galaxy containing our Solar System.', 100, 8, TRUE),
universe->     ('Andromeda', 'The nearest spiral galaxy to the Milky Way.', 200, 10, FALSE),
universe->     ('Triangulum', 'The third-largest galaxy in the Local Group.', 50, 5, FALSE),
universe->     ('Messier 87', 'A supergiant elliptical galaxy in the Virgo constellation.', 300, 15, TRUE),
universe->     ('Sombrero', 'A spiral galaxy in the constellation Virgo.', 70, 7, FALSE),
universe->     ('Pinwheel', 'A face-on spiral galaxy in the constellation Ursa Major.', 80, 6, FALSE);
INSERT 0 6
universe=> CREATE TABLE star (
universe(>     star_id SERIAL PRIMARY KEY,
universe(>     name VARCHAR NOT NULL UNIQUE,
universe(>     description TEXT,
universe(>     galaxy_id INT NOT NULL,
universe(>     temperature NUMERIC,
universe(>     is_binary BOOLEAN,
universe(>     CONSTRAINT fk_galaxy_id FOREIGN KEY (galaxy_id) REFERENCES galaxy(galaxy_id)
universe(> );
CREATE TABLE
universe=> INSERT INTO star (name, description, galaxy_id, temperature, is_binary)
universe-> VALUES
universe->     ('Sun', 'The star at the center of the Solar System.', 1, 5778, FALSE),
universe->     ('Sirius', 'The brightest star in the night sky.', 2, 9940, FALSE),
universe->     ('Betelgeuse', 'A red supergiant star in the constellation of Orion.', 3, 3500, FALSE),
universe->     ('Proxima Centauri', 'The closest known star to the Sun.', 1, 3042, FALSE),
universe->     ('Alpha Centauri A', 'A binary star system in the constellation of Centaurus.', 1, 5790, TRUE),
universe->     ('Alpha Centauri B', 'A binary star system in the constellation of Centaurus.', 1, 5260, TRUE);
INSERT 0 6
universe=> CREATE TABLE planet (
universe(>     planet_id SERIAL PRIMARY KEY,
universe(>     name VARCHAR NOT NULL UNIQUE,
universe(>     description TEXT,
universe(>     star_id INT NOT NULL,
universe(>     radius NUMERIC,
universe(>     has_water BOOLEAN,
universe(>     CONSTRAINT fk_star_id FOREIGN KEY (star_id) REFERENCES star(star_id)
universe(> );
CREATE TABLE
universe=> INSERT INTO planet (name, description, star_id, radius, has_water)
universe-> VALUES
universe->     ('Mercury', 'The smallest and innermost planet in the Solar System.', 1, 2439, FALSE),
universe->     ('Venus', 'The second planet from the Sun.', 1, 6052, TRUE),
universe->     ('Earth', 'The third planet from the Sun.', 1, 6371, TRUE),
universe->     ('Mars', 'The fourth planet from the Sun.', 1, 3390, FALSE),
universe->     ('Jupiter', 'The largest planet in the Solar System.', 2, 69911, FALSE),
universe->     ('Saturn', 'The sixth planet from the Sun.', 2, 58232, FALSE),
universe->     ('Uranus', 'The seventh planet from the Sun.', 2, 25362, FALSE),
universe->     ('Neptune', 'The eighth and farthest-known Solar planet from the Sun.', 2, 24622, FALSE),
universe->     ('Proxima Centauri b', 'An exoplanet orbiting the red dwarf star Proxima Centauri.', 4, 6052, TRUE),
universe->     ('Alpha Centauri Bb', 'An exoplanet orbiting the star Alpha Centauri B.', 6, 7990, FALSE),
universe->     ('Kepler-186f', 'An exoplanet orbiting the red dwarf star Kepler-186.', 3, 10321, TRUE),
universe->     ('TRAPPIST-1e', 'An exoplanet orbiting the ultracool dwarf star TRAPPIST-1.', 3, 7231, TRUE);
on (
    moon_id SERIAL PRIMARY KEY,
    name VARCHAR NOT NULL UNIQUE,
    description TEXT,
    plaINSERT 0 12
universe=> 
universe=> -- Create the "moon" table
universe=> CREATE TABLE moon (
universe(>     moon_id SERIAL PRIMARY KEY,
universe(>     name VARCHAR NOT NULL UNIQUE,
universe(>     description TEXT,
universe(>     planet_id INT NOT NULL,
universe(>     diameter NUMERIC,
universe(>     has_atmosphere BOOLEAN,
universe(>     CONSTRAINT fk_planet_id FOREIGN KEY (planet_id) REFERENCES planet(planet_id)
universe(> );
CREATE TABLE
universe=> 
universe=> 
universe=> INSERT INTO moon (name, description, planet_id, diameter, has_atmosphere)
universe-> VALUES
universe->     ('Moon', 'The Earth''s only natural satellite.', 3, 3474, FALSE),
universe->     ('Titan', 'The largest moon of Saturn.', 7, 5150, TRUE),
universe->     ('Europa', 'The smallest of the four Galilean moons orbiting Jupiter.', 5, 3121, TRUE),
universe->     ('Ganymede', 'The largest and most massive moon of Jupiter.', 5, 5262, TRUE),
universe->     ('Triton', 'The largest natural satellite of the planet Neptune.', 8, 2707, TRUE),
universe->     ('Enceladus', 'The sixth-largest moon of Saturn.', 6, 513, TRUE),
universe->     ('Io', 'The innermost and third-largest of the four Galilean moons of Jupiter.', 5, 3662, FALSE),
universe->     ('Callisto', 'The second-largest moon of Jupiter.', 5, 4821, FALSE),
universe->     ('Deimos', 'The smaller and outermost of the two natural satellites of the planet Mars.', 4, 10.2, FALSE),
universe->     ('Phobos', 'The larger and closer of the two natural satellites of Mars.', 4, 22.2, FALSE),
universe->     ('Charon', 'The largest of the five known moons of the dwarf planet Pluto.', 9, 1208, TRUE),
universe->     ('Luna', 'The Roman divine personification of the Moon.', 3, 3474, FALSE),
universe->    ('Oberon', 'The outermost of the major moons of Uranus.', 7, 1523, FALSE),
universe->     ('Rhea', 'The second-largest moon of Saturn.', 6, 1528, FALSE),
universe->     ('Miranda', 'The smallest and innermost of Uranus''s five major moons.', 7, 472, FALSE),
universe->     ('Titania', 'The largest moon of Uranus.', 7, 1578, FALSE),
universe->     ('Ariel', 'The fourth-largest moon of Uranus.', 7, 1158, FALSE),
universe->     ('Dione', 'The third-largest moon of Saturn.', 6, 1123, FALSE),
universe->     ('Mimas', 'A moon of Saturn which was discovered in 1789.', 6, 396, FALSE),
universe->     ('Iapetus', 'The third-largest natural satellite of Saturn.', 6, 1470, FALSE),
universe->     ('Tethys', 'A moon of Saturn which was discovered by Giovanni Domenico Cassini in 1684.', 6, 1062, FALSE),
universe->     ('Umbriel', 'A moon of Uranus which was discovered by William Lassell in 1851.', 7, 1169, FALSE);
INSERT 0 22
universe=> CREATE TABLE quantum (
universe(>     quantum_id SERIAL PRIMARY KEY,
universe(>     name VARCHAR NOT NULL,
universe(>     description TEXT,
universe(>     text_column TEXT NOT NULL,
universe(>     unique_name VARCHAR UNIQUE NOT NULL
universe(> );
CREATE TABLE
universe=> INSERT INTO quantum (name, description, text_column, unique_name)
universe-> VALUES
universe->     ('Electron', 'Elementary particle with a negative elementary charge.', 'An electron is a subatomic particle that carries a negative electric charge.', 'Electron1'),
universe->     ('Photon', 'Elementary particle representing a quantum of light and other electromagnetic radiation.', 'A photon is an elementary particle, the quantum of the electromagnetic field including electromagnetic radiation such as light.', 'Photon1'),
universe->     ('Quark', 'Elementary particle and a fundamental constituent of matter.', 'A quark is a type of elementary particle and a fundamental constituent of matter.', 'Quark1'),
universe->     ('Neutrino', 'Elementary particle similar to the electron but with much smaller mass.', 'A neutrino is a subatomic particle that is very similar to an electron, but has no electrical charge and a very small mass.', 'Neutrino1'),
universe->     ('Boson', 'A particle that mediates the fundamental forces of nature.', 'A boson is a subatomic particle that mediates the fundamental forces of nature.', 'Boson1'),
universe->     ('Graviton', 'The hypothetical elementary particle that mediates the force of gravitation in the framework of quantum field theory.', 'A graviton is a hypothetical elementary particle that mediates the force of gravitation in the framework of quantum field theory.', 'Graviton1');
INSERT 0 6
universe=> 
