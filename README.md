# Chudo_Yudo
create table roles(
	id serial primary key,
	name varchar
);

create table manufactures(
	id serial primary key,
	name varchar
);

create table categories(
	id serial primary key,
	name varchar
);

create table subcategories(
	id serial primary key,
	name varchar
);

create table sizes (
	id serial primary key,
	name varchar
);

create table users(
	id serial primary key,
	name varchar,
	surname varchar,
	lastname varchar,
	otchestvo varchar,
	id_role int references roles(id)
 );

create table products(
	id serial primary key,
	id_category int references categories(id),
	id_subcategory int references subcategories(id),
	img varchar,
	name varchar,
	id_manufacture int references manufactures(id),
	description varchar,
	structure varchar,
	price float
);

create table stocks(
	id serial primary key,
	id_product int references products(id),
	id_sizes int references sizes(id),
	count int
);

create table orders(
	id serial primary key,
	dateOfOrders date,
	id_user int references users(id)
);

create table order_items(
	id serial primary key,
	id_orders int references orders(id),
	id_stock int references stocks(id),
	count int
);

=индекс($N:$N;поискпоз(E2;$O:$O;0))
=I1&" "&J1&" "&K1
Binary paths /usr/bin
# Chudo_Yudo
