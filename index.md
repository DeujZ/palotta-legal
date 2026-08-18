# Politique de confidentialité — Frigy

**Dernière mise à jour : 18 août 2026**
**Version : 1.0**

---

## 1. En résumé

Frigy est conçue pour fonctionner sans compte utilisateur et sans collecte de données personnelles identifiantes.

- Nous ne vous demandons ni nom, ni adresse e-mail, ni numéro de téléphone.
- Vos listes de courses, votre garde-manger et vos recettes sont enregistrés **uniquement sur votre appareil**.
- Nous ne consultons pas ces données et n'y avons pas accès.
- Nous ne vendons, ne louons et ne partageons aucune donnée à des fins publicitaires.
- Frigy ne contient aucun outil de mesure d'audience, de publicité ou de suivi comportemental.

Les seules données qui quittent votre appareil sont celles nécessaires à l'analyse d'un ticket de caisse ou à la génération d'une suggestion de recette, au moment précis où vous déclenchez ces actions.

---

## 2. Responsable du traitement

Rafael Lima
Suisse

Contact : rafael.tech2190@gmail.com

Pour toute question relative à cette politique ou au traitement de vos données, vous pouvez écrire à cette adresse.

---

## 3. Données enregistrées sur votre appareil

Frigy enregistre dans la mémoire locale de votre téléphone l'ensemble des informations nécessaires à son fonctionnement, à savoir :

- **le contenu de votre garde-manger** : les articles que vous possédez, leur quantité et leur unité ;
- **votre liste de courses** : les articles à acheter et leur état ;
- **vos recettes** : celles que vous avez enregistrées, mises en favori ou marquées à faire ;
- **vos préférences alimentaires** : le régime alimentaire éventuellement sélectionné ;
- **les données techniques de fonctionnement** : suggestions de recettes déjà consultées et conservées pour éviter de les recalculer, numéro de version déjà vu afin de n'afficher les nouveautés qu'une seule fois, et vos réglages d'application.

Aucune autre catégorie de données n'est enregistrée. En particulier, Frigy n'enregistre ni identité, ni coordonnées, ni historique de navigation, ni données de localisation.

Ces données :

- restent sur votre appareil et ne sont transmises à aucun serveur pour y être stockées ;
- ne sont associées à aucun identifiant de compte, puisque Frigy n'en utilise pas ;
- sont **intégralement supprimées lorsque vous désinstallez l'application**.

Ces informations peuvent être incluses dans les sauvegardes automatiques de votre téléphone (iCloud, Google), selon les réglages de votre appareil. Ces sauvegardes relèvent d'Apple ou de Google et de leurs propres conditions.

---

## 4. Données transmises hors de votre appareil

Trois types de transmission, et trois seulement, font sortir des données de votre appareil.

### 4.1 Le scan d'un ticket de caisse

Lorsque vous photographiez ou importez un ticket :

1. L'image est redimensionnée et compressée sur votre téléphone.
2. Elle est envoyée à notre serveur, qui la conserve **uniquement en mémoire vive**, sans jamais l'écrire sur disque.
3. Elle est transmise à l'API d'Anthropic pour en extraire la liste des articles.
4. La liste extraite vous est renvoyée, puis l'image **n'est jamais conservée après la fin de la requête**.

**Aucune photo de ticket n'est conservée, ni sur nos serveurs, ni ailleurs.**

Un ticket de caisse peut contenir des informations indirectes vous concernant : nom de l'enseigne, date, heure, montant total, moyen de paiement, et parfois un numéro de carte de fidélité. L'image complète du ticket est transmise pour analyse — nous ne pouvons pas masquer ces éléments avant l'envoi. En revanche, **seuls les articles alimentaires sont extraits et conservés**, uniquement sur votre appareil. Aucun autre élément du ticket n'est retenu ni enregistré, hors cas d'erreur technique de traitement (voir section 5).

Si vous souhaitez éviter la transmission de ces informations, vous pouvez masquer physiquement les parties concernées du ticket avant de le photographier, ou saisir vos articles manuellement.

### 4.2 Les suggestions de recettes

Lorsque vous demandez des suggestions, la liste des ingrédients disponibles dans votre garde-manger, ainsi que votre régime alimentaire s'il est renseigné, sont transmis à notre serveur puis à l'API d'Anthropic pour générer les propositions. Ces informations ne sont pas conservées après traitement.

Un régime alimentaire peut, dans certains cas, refléter une conviction personnelle ou une contrainte de santé. Cette information n'est transmise que lorsque vous demandez des suggestions, n'est associée à aucune identité, et n'est conservée que sur votre appareil.

### 4.3 La recherche de mises à jour

À chaque démarrage, l'application interroge automatiquement les serveurs d'Expo pour vérifier l'existence d'une mise à jour. Cette requête transmet des informations techniques (identifiant du projet, version installée, type d'appareil) ainsi que votre adresse IP. Elle ne contient aucune de vos données personnelles ni aucun contenu de l'application.

---

## 5. Journaux techniques

Notre serveur produit des journaux d'exploitation, hébergés chez Render.

**En fonctionnement normal**, ils ne contiennent que des données techniques anonymes : durées de traitement, nombre d'articles détectés, tailles de fichiers.

**Dans deux situations particulières**, des éléments supplémentaires peuvent y apparaître :

- **En cas d'erreur d'analyse** : un fragment du contenu extrait du ticket peut être enregistré afin de diagnostiquer le problème.
- **En cas de dépassement du nombre de requêtes autorisées** : votre adresse IP peut être enregistrée.

Par ailleurs, un mécanisme de limitation du débit conserve temporairement votre adresse IP en mémoire vive, associée à un compteur de requêtes, pendant une durée maximale d'une heure. Cette information n'est jamais écrite sur disque, n'est associée à aucune autre donnée, et disparaît à chaque redémarrage du serveur.

---

## 6. Prestataires

Nous faisons appel aux prestataires suivants, agissant comme sous-traitants au sens de la législation applicable :

| Prestataire | Rôle | Localisation |
|---|---|---|
| **Anthropic PBC** | Analyse des tickets et génération des suggestions de recettes | États-Unis |
| **Render Services, Inc.** | Hébergement du serveur applicatif | États-Unis (société), serveurs en Europe |
| **Expo (650 Industries, Inc.)** | Diffusion des mises à jour de l'application | États-Unis |

Les données transmises à Anthropic dans le cadre de l'API ne sont pas utilisées pour entraîner ses modèles.

Ces transferts vers les États-Unis impliquent un régime de protection des données différent de celui applicable en Suisse et dans l'Union européenne. Nous limitons ces transmissions au strict nécessaire et à la durée du traitement.

---

## 7. Autorisations demandées par l'application

| Autorisation | Usage |
|---|---|
| **Appareil photo** | Photographier un ticket de caisse. Utilisée uniquement pendant que l'écran de scan est ouvert. |
| **Capteurs de mouvement** (iOS) | Déclencher automatiquement la photo lorsque le téléphone est stable. Aucune donnée de mouvement n'est enregistrée ni transmise. |
| **Sélection d'une image** | L'application utilise le sélecteur d'images du système. Elle ne reçoit que l'image que vous avez explicitement choisie et n'a **aucun accès** au reste de votre galerie. |

---

## 8. Publicité, mesure d'audience et revente

Frigy ne contient :

- aucune régie publicitaire ;
- aucun outil de mesure d'audience ou d'analyse comportementale ;
- aucun traceur ni cookie publicitaire ;
- aucun dispositif de profilage ou de décision automatisée produisant des effets juridiques à votre égard.

Aucune donnée n'est vendue, louée ou cédée à des tiers.

---

## 9. Durées de conservation

| Donnée | Durée |
|---|---|
| Données de l'application (garde-manger, listes, recettes, préférences) | Jusqu'à la désinstallation, sous votre contrôle |
| Image d'un ticket | Le temps du traitement uniquement, jamais conservée |
| Adresse IP (limitation de débit) | Une heure maximum, en mémoire vive |
| Journaux techniques | Selon la politique de rétention de notre hébergeur |

---

## 10. Vos droits

Conformément à la loi fédérale suisse sur la protection des données (nLPD) et, lorsque vous résidez dans l'Union européenne, au Règlement général sur la protection des données (RGPD), vous disposez d'un droit d'accès, de rectification, d'effacement, d'opposition et de portabilité.

**En pratique**, puisque Frigy ne détient aucun compte ni aucune donnée vous identifiant sur ses serveurs :

- **Accès et portabilité** : vos données sont visibles à tout moment dans l'application, sur votre appareil.
- **Rectification** : vous pouvez modifier ou supprimer chaque élément directement dans l'application.
- **Effacement** : désinstaller l'application supprime définitivement l'ensemble de vos données.

Pour toute demande relative à ces droits, écrivez-nous à rafael.tech2190@gmail.com. Nous répondons dans un délai de trente jours.

Si vous estimez que le traitement de vos données n'est pas conforme, vous pouvez saisir le Préposé fédéral à la protection des données et à la transparence (PFPDT), Feldeggweg 1, 3003 Berne, Suisse. Si vous résidez dans l'Union européenne, vous pouvez saisir l'autorité de contrôle de votre pays de résidence.

---

## 11. Sécurité

Les échanges entre l'application et notre serveur sont chiffrés (HTTPS). L'accès à notre serveur est limité par un mécanisme de contrôle et une limitation du nombre de requêtes.

Aucune transmission sur internet ne pouvant être garantie totalement sûre, nous nous engageons à mettre en œuvre des mesures proportionnées au regard des données concernées, qui sont limitées à des informations alimentaires non identifiantes.

---

## 12. Mineurs

Frigy n'est pas destinée spécifiquement aux enfants et ne collecte sciemment aucune donnée les concernant. L'application ne demandant ni identité ni âge, elle ne traite aucune donnée permettant d'identifier un utilisateur, quel que soit son âge.

---

## 13. Modifications de cette politique

Cette politique pourra évoluer, notamment lors de l'ajout de nouvelles fonctionnalités. Toute modification substantielle — en particulier l'introduction de comptes utilisateurs et du partage de listes entre plusieurs personnes — fera l'objet d'une mise à jour de ce document et d'une information dans l'application.

La date de dernière mise à jour figure en tête de ce document.

---

## 14. Contact

rafael.tech2190@gmail.com
