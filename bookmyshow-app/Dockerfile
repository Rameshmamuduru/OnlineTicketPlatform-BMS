FROM node:18-alphine AS build
WORKDIR /app
COPY package.json package-lock.json ./

# Force install a compatible PostCSS version to fix the issue
RUN npm install postcss@8.4.21 postcss-safe-parser@6.0.0 --legacy-peer-deps

# Install dependencies
RUN npm install
COPY . .
RUN npm run build

FROM nginx:alphine
COPY --from=build app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
