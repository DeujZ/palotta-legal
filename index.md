---
title: Politique de confidentialité — Palotta
---

# Politique de confidentialité — Palotta

**Dernière mise à jour : 22 septembre 2026** **Version : 2.0**

---

## 1. En résumé

Palotta est une application de gestion de garde-manger et de listes de courses. Contrairement à ce qu'indiquait une version antérieure de ce document, **Palotta utilise désormais un compte pour synchroniser vos données entre vos appareils et vous permettre de les récupérer en cas de changement de téléphone.**

- Dès la première ouverture de l'application, un identifiant de compte est créé automatiquement, sans que vous ayez à saisir quoi que ce soit. Cet identifiant n'est associé à aucune information vous identifiant personnellement.
- Vous pouvez, si vous le souhaitez, rattacher une adresse e-mail à ce compte pour vous reconnecter sur un autre appareil. Aucun mot de passe n'est utilisé : la connexion se fait par un code à 6 chiffres envoyé par e-mail.
- Votre garde-manger et votre liste de courses sont enregistrés à la fois sur votre appareil et sur nos serveurs (Supabase, hébergés en Suisse), afin de rester disponibles même si vous changez de téléphone ou désinstallez l'application par erreur.
- Vos recettes et vos préférences alimentaires restent enregistrées uniquement sur votre appareil.
- Nous ne vendons, ne louons et ne partageons aucune donnée à des fins publicitaires. Palotta ne contient aucun outil de mesure d'audience, de publicité ou de suivi comportemental.
- Vous pouvez supprimer définitivement votre compte et l'ensemble des données associées directement depuis l'application, à tout moment.

Les autres données qui quittent votre appareil sont celles nécessaires à l'analyse d'un ticket de caisse ou à la génération d'une suggestion de recette, au moment précis où vous déclenchez ces actions.

---

## 2. Responsable du traitement

Rafael Lima
Suisse

Contact : contact@palotta.ch

Pour toute question relative à cette politique ou au traitement de vos données, vous pouvez écrire à cette adresse.

---

## 3. Votre compte

### 3.1 Compte créé automatiquement

Dès que vous ouvrez l'application pour la première fois, un compte est créé automatiquement sur nos serveurs, sans action de votre part. Ce compte n'est associé à aucune adresse e-mail ni aucune information vous identifiant : il consiste en un identifiant technique unique, généré au hasard, qui nous permet de savoir quelles données de garde-manger et de liste de courses vous appartiennent.

### 3.2 Compte avec adresse e-mail (facultatif)

Vous pouvez, à tout moment, rattacher une adresse e-mail à votre compte. Cette étape est facultative : l'application reste pleinement fonctionnelle sans elle. Elle sert uniquement à vous permettre de retrouver vos données si vous changez de téléphone.

La connexion se fait par un code à 6 chiffres envoyé à votre adresse e-mail — nous n'utilisons ni ne stockons aucun mot de passe.

### 3.3 Suppression de votre compte

Vous pouvez supprimer votre compte à tout moment depuis l'application (section « Mon compte »). Cette action est **immédiate et définitive** : elle supprime votre adresse e-mail (si vous en aviez rattaché une), votre garde-manger, votre liste de courses et l'historique technique de synchronisation, sur nos serveurs comme sur votre appareil. Aucune période de grâce ni de récupération n'est possible après confirmation.

---

## 4. Données enregistrées

### 4.1 Sur votre appareil et sur nos serveurs

- **le contenu de votre garde-manger** : les articles que vous possédez, leur quantité et leur unité ;
- **votre liste de courses** : les articles à acheter et leur état.

Ces données sont enregistrées localement pour un accès instantané, même hors connexion, puis synchronisées avec nos serveurs (Supabase, hébergés en Suisse) dès que votre appareil retrouve une connexion réseau. Elles sont associées uniquement à l'identifiant de compte décrit à la section 3, jamais à votre nom ou à votre adresse e-mail directement.

### 4.2 Uniquement sur votre appareil

- **vos recettes** : celles que vous avez enregistrées, mises en favori ou marquées à faire ;
- **vos préférences alimentaires** : le régime alimentaire éventuellement sélectionné ;
- **les données techniques de fonctionnement** : suggestions de recettes déjà consultées et conservées pour éviter de les recalculer, numéro de version déjà vu afin de n'afficher les nouveautés qu'une seule fois, et vos réglages d'application.

Ces données ne sont transmises à aucun serveur pour y être stockées de façon durable, et sont supprimées lorsque vous désinstallez l'application ou supprimez votre compte.

Ces informations peuvent être incluses dans les sauvegardes automatiques de votre téléphone (iCloud, Google), selon les réglages de votre appareil. Ces sauvegardes relèvent d'Apple ou de Google et de leurs propres conditions.

---

## 5. Données transmises pour analyse

Trois types de transmission, en plus de la synchronisation décrite à la section 4.1, font sortir des données de votre appareil.

### 5.1 Le scan d'un ticket de caisse

Lorsque vous photographiez ou importez un ticket :

1. L'image est redimensionnée et compressée sur votre téléphone.
2. Elle est envoyée à notre serveur, qui la conserve **uniquement en mémoire vive**, sans jamais l'écrire sur disque.
3. Elle est transmise à l'API d'Anthropic pour en extraire la liste des articles.
4. La liste extraite vous est renvoyée, puis l'image **n'est jamais conservée après la fin de la requête**.

**Aucune photo de ticket n'est conservée, ni sur nos serveurs, ni ailleurs.**

Un ticket de caisse peut contenir des informations indirectes vous concernant : nom de l'enseigne, date, heure, montant total, moyen de paiement, et parfois un numéro de carte de fidélité. L'image complète du ticket est transmise pour analyse — nous ne pouvons pas masquer ces éléments avant l'envoi. En revanche, **seuls les articles alimentaires sont extraits et conservés**, dans votre garde-manger tel que décrit à la section 4.1. Aucun autre élément du ticket n'est retenu ni enregistré, hors cas d'erreur technique de traitement (voir section 6).

Si vous souhaitez éviter la transmission de ces informations, vous pouvez masquer physiquement les parties concernées du ticket avant de le photographier, ou saisir vos articles manuellement.

### 5.2 Les suggestions de recettes

Lorsque vous demandez des suggestions, la liste des ingrédients disponibles dans votre garde-manger, ainsi que votre régime alimentaire s'il est renseigné, sont transmis à notre serveur puis à l'API d'Anthropic pour générer les propositions. Ces informations ne sont pas conservées après traitement par Anthropic.

Un régime alimentaire peut, dans certains cas, refléter une conviction personnelle ou une contrainte de santé. Cette information n'est transmise que lorsque vous demandez des suggestions, et n'est conservée durablement que sur votre appareil (section 4.2).

### 5.3 La recherche de mises à jour

À chaque démarrage, l'application interroge automatiquement les serveurs d'Expo pour vérifier l'existence d'une mise à jour. Cette requête transmet des informations techniques (identifiant du projet, version installée, type d'appareil) ainsi que votre adresse IP. Elle ne contient aucune de vos données personnelles ni aucun contenu de l'application.

---

## 6. Journaux techniques

Notre serveur produit des journaux d'exploitation, hébergés chez Render.

**En fonctionnement normal**, ils ne contiennent que des données techniques anonymes : durées de traitement, nombre d'articles détectés, tailles de fichiers, compteurs d'éléments supprimés lors d'une suppression de compte. Le contenu de vos articles ou de vos e-mails n'y figure jamais.

**Dans deux situations particulières**, des éléments supplémentaires peuvent y apparaître :

- **En cas d'erreur d'analyse** : un fragment du contenu extrait du ticket peut être enregistré afin de diagnostiquer le problème.
- **En cas de dépassement du nombre de requêtes autorisées** : votre adresse IP peut être enregistrée.

Par ailleurs, un mécanisme de limitation du débit conserve temporairement votre adresse IP en mémoire vive, associée à un compteur de requêtes, pendant une durée maximale d'une heure. Cette information n'est jamais écrite sur disque, n'est associée à aucune autre donnée, et disparaît à chaque redémarrage du serveur.

---

## 7. Prestataires

Nous faisons appel aux prestataires suivants, agissant comme sous-traitants au sens de la législation applicable :

| Prestataire                     | Rôle                                                          | Localisation                             |
| -------------------------------- | -------------------------------------------------------------- | ----------------------------------------- |
| **Supabase Inc.**                | Hébergement de votre compte et de vos données de garde-manger/liste de courses | Serveurs en Suisse (Zurich)              |
| **Anthropic PBC**                | Analyse des tickets et génération des suggestions de recettes  | États-Unis                                |
| **Render Services, Inc.**        | Hébergement du serveur applicatif                               | États-Unis (société), serveurs en Europe |
| **Resend**                       | Envoi des e-mails contenant votre code de connexion             | États-Unis                                |
| **Expo (650 Industries, Inc.)**  | Diffusion des mises à jour de l'application                     | États-Unis                                |

Les données transmises à Anthropic dans le cadre de l'API ne sont pas utilisées pour entraîner ses modèles.

Les transferts vers les États-Unis impliquent un régime de protection des données différent de celui applicable en Suisse et dans l'Union européenne. Nous limitons ces transmissions au strict nécessaire et à la durée du traitement.

---

## 8. Autorisations demandées par l'application

| Autorisation                    | Usage                                                                                                                                                                    |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Appareil photo**               | Photographier un ticket de caisse. Utilisée uniquement pendant que l'écran de scan est ouvert.                                                                           |
| **Capteurs de mouvement** (iOS)  | Déclencher automatiquement la photo lorsque le téléphone est stable. Aucune donnée de mouvement n'est enregistrée ni transmise.                                          |
| **Sélection d'une image**        | L'application utilise le sélecteur d'images du système. Elle ne reçoit que l'image que vous avez explicitement choisie et n'a **aucun accès** au reste de votre galerie. |

---

## 9. Publicité, mesure d'audience et revente

Palotta ne contient :

- aucune régie publicitaire ;
- aucun outil de mesure d'audience ou d'analyse comportementale ;
- aucun traceur ni cookie publicitaire ;
- aucun dispositif de profilage ou de décision automatisée produisant des effets juridiques à votre égard.

Aucune donnée n'est vendue, louée ou cédée à des tiers.

---

## 10. Durées de conservation

| Donnée                                                                  | Durée                                                                |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------- |
| Garde-manger et liste de courses (appareil et serveur)                   | Jusqu'à suppression de l'article, désinstallation, ou suppression du compte |
| Compte (identifiant, adresse e-mail si rattachée)                        | Jusqu'à suppression volontaire du compte — immédiate et définitive     |
| Recettes et préférences alimentaires                                     | Jusqu'à désinstallation, sous votre contrôle                            |
| Image d'un ticket                                                        | Le temps du traitement uniquement, jamais conservée                    |
| Adresse IP (limitation de débit)                                         | Une heure maximum, en mémoire vive                                     |
| Journaux techniques                                                      | Selon la politique de rétention de notre hébergeur                     |

---

## 11. Vos droits

Conformément à la loi fédérale suisse sur la protection des données (nLPD) et, lorsque vous résidez dans l'Union européenne, au Règlement général sur la protection des données (RGPD), vous disposez d'un droit d'accès, de rectification, d'effacement, d'opposition et de portabilité.

**En pratique :**

- **Accès et rectification** : vos données de garde-manger et de liste de courses sont visibles et modifiables à tout moment dans l'application.
- **Effacement** : vous pouvez supprimer votre compte et l'ensemble des données associées directement depuis l'application (section « Mon compte »). Cette action est immédiate et définitive.
- **Portabilité (export de vos données)** : cette fonctionnalité n'est pas encore automatisée dans l'application. Pour recevoir une copie de vos données, écrivez-nous à contact@palotta.ch en précisant l'adresse e-mail associée à votre compte (ou l'identifiant technique si vous n'en avez pas rattaché). Nous vous répondons dans un délai de trente jours.
- **Opposition** : vous pouvez à tout moment cesser d'utiliser les fonctionnalités reposant sur l'analyse de tickets ou la suggestion de recettes sans que cela affecte le reste de l'application.

Si vous estimez que le traitement de vos données n'est pas conforme, vous pouvez saisir le Préposé fédéral à la protection des données et à la transparence (PFPDT), Feldeggweg 1, 3003 Berne, Suisse. Si vous résidez dans l'Union européenne, vous pouvez saisir l'autorité de contrôle de votre pays de résidence.

---

## 12. Sécurité

Les échanges entre l'application et nos serveurs sont chiffrés (HTTPS). L'accès à votre compte et à vos données est protégé par un code de connexion à usage unique valable une durée limitée — nous n'utilisons aucun mot de passe, qui ne peut donc pas être volé ou deviné. Une règle de sécurité au niveau de la base de données (Row Level Security) garantit que personne ne peut consulter les données d'un autre compte que le sien, y compris en cas de faille applicative.

Aucune transmission sur internet ne pouvant être garantie totalement sûre, nous nous engageons à mettre en œuvre des mesures proportionnées au regard des données concernées.

---

## 13. Mineurs

Palotta n'est pas destinée spécifiquement aux enfants et ne collecte sciemment aucune donnée les concernant. L'application ne demandant aucune information d'âge, elle ne traite aucune donnée permettant de déterminer l'âge d'un utilisateur.

---

## 14. Modifications de cette politique

Cette politique a évolué le 22 septembre 2026 pour refléter l'introduction d'un compte utilisateur et de la synchronisation de vos données de garde-manger et de liste de courses. Une version antérieure de ce document indiquait qu'aucune donnée n'était stockée sur nos serveurs : cette affirmation ne reflétait plus la réalité depuis l'introduction de la synchronisation, et a été corrigée à cette occasion.

Cette politique pourra encore évoluer, notamment lors de l'introduction du partage de listes entre plusieurs personnes. Toute modification substantielle fera l'objet d'une nouvelle mise à jour de ce document et d'une information dans l'application.

La date de dernière mise à jour figure en tête de ce document.

---

## 15. Contact

contact@palotta.ch
