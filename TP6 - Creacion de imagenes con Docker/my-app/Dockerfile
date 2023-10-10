#build stage
FROM node:13.12.0-alpine AS build
WORKDIR /app
COPY /package*.json ./
RUN npm install
COPY . .

#produccion stage
FROM node:13.12.0-alpine 
WORKDIR /app
COPY --from=build /app ./
EXPOSE 3000
CMD ["npm", "start"]

