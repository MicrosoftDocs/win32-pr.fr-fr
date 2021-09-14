---
description: Répertorie les valeurs retournées par les fonctions de gestion de la sécurité.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valeurs de retour de la gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193760"
---
# <a name="security-management-return-values"></a>Valeurs de retour de la gestion de la sécurité

Les valeurs de retour de la gestion de la sécurité sont les suivantes :

-   [Valeurs de retour des pièces jointes](#attachment-return-values)
-   [Valeurs de retour de la fonction de stratégie LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valeurs de retour des pièces jointes

L’ensemble d’outils de configuration de la sécurité prend en charge les codes de retour **SCESTATUS** suivants. Ces valeurs sont retournées par les fonctions de prise en charge des pièces jointes et les fonctions implémentées lors de l’écriture d’un moteur ou d’un composant logiciel enfichable.



| Valeur                            | Description                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| réussite de SCESTATUS \_               | La fonction a réussi.                                                                          |
| \_paramètre SCESTATUS non valide \_    | L’un des paramètres passés à la fonction n’est pas valide.                                      |
| \_enregistrement SCESTATUS \_ \_ introuvable    | L’enregistrement spécifié est introuvable dans la base de données de sécurité.                                     |
| SCESTATUS des \_ données non valides \_         | La fonction a échoué, car certaines données n’étaient pas valides.                                             |
| l' \_ objet SCESTATUS \_ existe        | L'objet existe déjà.                                                                       |
| \_mémoire tampon SCESTATUS \_ trop \_ petite    | La mémoire tampon transmise à la fonction pour recevoir des données n’est pas assez grande pour recevoir toutes les données. |
| \_Profil SCESTATUS \_ \_ introuvable   | Le profil spécifié est introuvable.                                                             |
| \_format incorrect SCESTATUS \_           | Le format n’est pas valide.                                                                         |
| SCESTATUS \_ de \_ ressources insuffisantes \_ | La mémoire est insuffisante.                                                                    |
| \_accès SCESTATUS \_ refusé        | L’appelant ne dispose pas de privilèges suffisants pour effectuer cette action.                          |
| SCESTATUS \_ Impossible de \_ Supprimer          | La fonction ne peut pas supprimer l’élément spécifié.                                                   |
| \_dépassement du préfixe SCESTATUS \_      | Un dépassement de préfixe s’est produit.                                                                      |
| SCESTATUS \_ autre \_ erreur          | Une erreur inconnue s’est produite.                                                               |
| SCESTATUS \_ déjà \_ en cours d’exécution      | Le service est déjà en cours d'exécution.                                                                  |
| \_service SCESTATUS \_ non \_ pris en charge | Le service spécifié n’est pas pris en charge.                                                          |
| SCESTATUS \_ Mod \_ \_ introuvable       | Impossible de trouver ou de charger une DLL du moteur de pièce jointe figurant dans le registre.      |
| \_exception SCESTATUS \_ dans le \_ serveur | Une exception s’est produite sur le serveur.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valeurs de retour de la fonction de stratégie LSA

La plupart des fonctions de stratégie de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) retournent une valeur NTSTATUS pour indiquer la réussite ou l’échec. les différentes valeurs ntstatus sont définies dans NTSTATUS. h, qui est distribué avec le kit de développement de pilotes (DDK) de Microsoft Windows.

pour convertir une valeur de retour NTSTATUS en code d’erreur Windows, utilisez la fonction [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) .

Le tableau suivant répertorie les valeurs NTSTATUS qui peuvent être retournées par toute fonction LSA. (Les sections de valeur de retour pour certaines des fonctions LSA répertorient les codes d’erreur supplémentaires que la fonction peut retourner.) ce tableau répertorie également le code d’erreur Windows qui correspond à chaque valeur NTSTATUS.



| code NTSTATUS (code d’erreur Windows)                                        | Signification                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| ÉTAT \_ de réussite (erreur de \_ réussite)<br/>                               | La fonction a réussi.                                                                                                            |
| \_accès à l’état \_ refusé (erreur \_ accès \_ refusé)<br/>                 | L’appelant ne dispose pas de l’accès approprié pour terminer l’opération.                                                                  |
| État des \_ ressources insuffisantes \_ (erreur \_ aucune \_ \_ ressource système)<br/> | Il n’y a pas assez de ressources système (telles que la mémoire pour allouer des tampons) pour terminer l’appel.                                        |
| \_ \_ erreur de base de la base de l’état interne \_ (erreur interne de la \_ \_ base de \_<br/>       | La base de données LSA contient une incohérence interne.                                                                                    |
| descripteur d’état \_ non valide \_ (erreur de \_ handle non valide \_ )<br/>               | Indique qu’un objet ou un handle RPC n’est pas valide dans le [*contexte*](/windows/desktop/SecGloss/c-gly) utilisé.     |
| état \_ du \_ serveur non valide \_ (erreur d’État du \_ serveur non valide \_ \_ )<br/> | Indique que le serveur LSA est actuellement désactivé.                                                                                         |
| paramètre d’état \_ non valide \_ (paramètre d’erreur \_ non valide \_ )<br/>         | L’un des paramètres n’est pas valide.                                                                                                     |
| ÉTAT \_ non \_ \_ privilégié (erreur non liée à \_ \_ ce type de \_ privilège)<br/>       | Indique qu’il n’existe pas de privilège spécifié.                                                                                         |
| \_nom de l’objet d’état \_ \_ \_ introuvable (fichier d’erreur \_ \_ \_ introuvable)<br/>     | Un objet dans la base de données de stratégie LSA est introuvable. L’objet a peut-être été spécifié par SID ou par nom, en fonction de son type. |
| État d' \_ échec (erreur de \_ génération d’erreur \_ )<br/>                     | Échec générique, tel que l’échec de la connexion RPC.                                                                                        |



 

 

