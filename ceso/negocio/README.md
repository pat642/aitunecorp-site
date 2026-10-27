# CESO · Negocio

Module commercial ajouté dans l'onglet Negocio du dashboard CESO existant. Aucune autre section remplacée. Les KPIs d'origine de Negocio restent dans un volet dépliable sous le CRM.

Le module est chargé à la demande dans une iframe de même origine pour isoler ses styles et scripts. Sa hauteur est communiquée à la page par postMessage avec vérification de l'origine et de la fenêtre source.

## Fonctionnement dans la publication statique

Données de démonstration fictives. Les modifications sont conservées uniquement dans le localStorage du navigateur, sous la clé `ceso-negocio-crm-v1`, sans synchronisation. Ce prototype public ne doit pas recevoir de données client réelles, de données médicales ou de secrets.

Le module comprend : actions du jour, entreprises et contacts, pipeline, préparation de brouillons, enregistrement de révisions locales, historique et export/restauration. Les montants sont des estimations commerciales ; aucune facturation ni aucun envoi de message n'est effectué.

Les révisions locales ne vérifient pas l'identité du relecteur. L'envoi de courriels, les réponses, WhatsApp et les permissions par utilisateur restent à connecter.

## Apollo

L'interface dispose d'un exemple fictif d'enrichissement et d'import avec contrôle des doublons. Une connexion réelle nécessite un serveur privé configuré avec les accès du compte CESO ; aucune clé n'est incluse dans ces fichiers. Le module détecte l'absence du serveur et l'indique explicitement. Endpoint serveur prévu : `/ceso-negocio-api/`.

La version locale complète, avec serveur Node 24, stockage SQLite, adaptateur Apollo et tests, est livrée séparément dans le dossier `ceso-comercial`. Elle n'est pas déployée sur l'hébergement statique du site vitrine.
