---
title: Mappage de l’interface utilisateur de l’unité d’organisation
description: Cette rubrique décrit les feuilles de propriétés d’objet de l’unité d’organisation (UO) dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d4f3e268e9448e9b835a4716cfa3f379ffb3cac93c2720e3f455a66384ed32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025517"
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
| Pays/Région  | [**Country-Name**](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a>Gestion par feuille de propriétés

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **géré par** .



| Étiquette d’interface utilisateur         | Attribut dans Active Directory Domain Services                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nom             | [**Géré par**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Office           | attribut [**physique-delivery-Office-name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) du compte identifié par **Name**. |
| Rue           | L’attribut [**rue-adresse**](/windows/desktop/ADSchema/a-street) du compte identifié par le **nom**.                                    |
| City             | Attribut de [**nom de localité**](/windows/desktop/ADSchema/a-l) du compte identifié par le **nom**.                                          |
| État/Province   | Attribut [**State-or-province-Name**](/windows/desktop/ADSchema/a-st) du compte identifié par **nom**.                                |
| Pays/région   | Attribut [**Country-Name**](/windows/desktop/ADSchema/a-c) du compte identifié par **Name**.                                           |
| Numéro de téléphone | Attribut de [**numéro de téléphone**](/windows/desktop/ADSchema/a-telephonenumber) du compte identifié par le **nom**.                         |
| Numéro de télécopie       | Attribut [**télécopie-numéro de téléphone**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) du compte identifié par le **nom**.      |



 

 

 