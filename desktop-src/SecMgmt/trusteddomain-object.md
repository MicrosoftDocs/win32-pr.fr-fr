---
description: L’objet TrustedDomain stocke les informations relatives à une relation d’approbation avec un domaine.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862297"
---
# <a name="trusteddomain-object"></a>Objet TrustedDomain

L’objet **trustedDomain** stocke les informations relatives à une relation d’approbation avec un domaine. Un objet **trustedDomain** est créé sur le système d’approbation pour identifier un compte au sein du domaine approuvé qui peut être utilisé pour envoyer des demandes d’authentification et effectuer d’autres opérations, telles que le nom et les traductions de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID).

Les informations stockées dans un objet **trustedDomain** incluent :

-   SID du domaine approuvé. Ces informations ne sont pas modifiables et doivent être uniques parmi tous les objets **trustedDomain** .
-   Nom du domaine approuvé. Ces informations ne sont pas modifiables et doivent être uniques parmi tous les objets **trustedDomain** .
-   Nom du compte dans le domaine approuvé utilisé pour soumettre les demandes d’authentification et pour effectuer des traductions de nom et SID. Ce nom n’est pas modifiable.
-   Mot de passe utilisé pour soumettre les demandes d’authentification et effectuer des traductions de nom et SID.

Pour plus d’informations, consultez [type d’objet trustedDomain](the-trusteddomain-object-type.md).

 

 
