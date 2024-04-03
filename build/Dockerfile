ARG KEYCLOAK_VERSION=base-image-tag
FROM bitnami/keycloak:${KEYCLOAK_VERSION}

COPY ./assets/localize /localize
ARG KEYCLOAK_VERSION
RUN jar uf "/opt/bitnami/keycloak/lib/lib/main/org.keycloak.keycloak-account-ui-${KEYCLOAK_VERSION}.jar" -C /localize/keycloak-account-ui theme
RUN jar uf "/opt/bitnami/keycloak/lib/lib/main/org.keycloak.keycloak-admin-ui-${KEYCLOAK_VERSION}.jar"   -C /localize/keycloak-admin-ui   theme
RUN jar uf "/opt/bitnami/keycloak/lib/lib/main/org.keycloak.keycloak-themes-${KEYCLOAK_VERSION}.jar"     -C /localize/keycloak-themes     theme
