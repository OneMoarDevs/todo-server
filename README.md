# todo-server


CREATE TYPE priority_enum AS ENUM ('low', 'medium', 'high');
CREATE TYPE category_enum AS ENUM ('chores', 'work', 'school', 'personal', 'others');

CREATE TABLE todos (id SERIAL PRIMARY KEY, title VARCHAR(255) NOT NULL, description TEXT, priority priority_enum NOT NULL, category category_enum NOT NULL, deadline DATE, completed BOOLEAN DEFAULT FALSE, created_at TIMESTAMP DEFAULT NOW());

INSERT INTO todos (title, description, priority, category) VALUES ('Task 1', 'Description 1', 'low', 'work');
