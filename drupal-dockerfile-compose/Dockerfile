FROM drupal
# Update the package list, install git, and clean up to minimize image size
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# Set the working directory to themes directory
WORKDIR /var/www/html/themes

# Correct the Git clone command with the proper repository and path handling
RUN git clone https://git.drupalcode.org/project/bootstrap.git && \
    chown -R www-data:www-data bootstrap

# Set the working directory back to the default Drupal root
WORKDIR /var/www/html
