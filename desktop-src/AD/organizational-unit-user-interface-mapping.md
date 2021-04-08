---
title: Mappage de l’interface utilisateur de l’unité d’organisation
description: Cette rubrique décrit les feuilles de propriétés d’objet de l’unité d’organisation (UO) dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8b08014d141c2182f47a5e3a40ebb9a18004ba
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842050"
---
# <a name="organizational-unit-user-interface-mapping"></a>Mappage de l’interface utilisateur de l’unité d’organisation

Cette rubrique décrit les feuilles de propriétés d’objet de l’unité d’organisation (UO) dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.

## <a name="general-property-sheet"></a>Feuille de propriétés général

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **générales** .



| Étiquette d’interface utilisateur        | Attribut dans Active Directory Domain Services |
|-----------------|-----------------------------------------------|
| Description     | [**Description**](/windows/desktop/ADSchema/a-description)     |
| Rue          | [**Rue-adresse**](/windows/desktop/ADSchema/a-street)       |
| City            | [**Localité-Name**](/windows/desktop/ADSchema/a-l)             |
| État/province  | [**Nom de l’État ou de la province**](/windows/desktop/ADSchema/a-st)   |
| Code postal | [**Code postal**](/windows/desktop/ADSchema/a-postalcode)      |
| Pays/région  | [**Country-Name**](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a>Gestion par feuille de propriétés

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **géré par** .



| Étiquette d’interface utilisateur         | Attribut dans Active Directory Domain Services                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nom             | [**Géré par**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Office           | Attribut [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) du compte identifié par **Name**. |
| Rue           | L’attribut [**rue-adresse**](/windows/desktop/ADSchema/a-street) du compte identifié par le **nom**.                                    |
| City             | Attribut de [**nom de localité**](/windows/desktop/ADSchema/a-l) du compte identifié par le **nom**.                                          |
| État/Province   | Attribut [**State-or-province-Name**](/windows/desktop/ADSchema/a-st) du compte identifié par **nom**.                                |
| Pays/région   | Attribut [**Country-Name**](/windows/desktop/ADSchema/a-c) du compte identifié par **Name**.                                           |
| Numéro de téléphone | Attribut de [**numéro de téléphone**](/windows/desktop/ADSchema/a-telephonenumber) du compte identifié par le **nom**.                         |
| Numéro de télécopie       | Attribut [**télécopie-numéro de téléphone**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) du compte identifié par le **nom**.      |



 

 

 