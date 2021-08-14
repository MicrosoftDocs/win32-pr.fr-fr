---
title: Mappage de l’interface utilisateur de l’objet de groupe
description: Cette rubrique décrit les feuilles de propriétés d’objet de groupe dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory. Propriété générale SheetMember de la propriété SheetMembers de la propriété SheetManaged par la feuille de propriétés
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Objet de groupe mappage de l’interface utilisateur Active Directory
- Mappage de l’interface utilisateur, objet groupe AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188963"
---
# <a name="group-object-user-interface-mapping"></a>Mappage de l’interface utilisateur de l’objet de groupe

Cette rubrique décrit les feuilles de propriétés d’objet de groupe dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.

-   [Feuille de propriétés général](#general-property-sheet)
-   [Membre de la feuille de propriétés](#member-of-property-sheet)
-   [Feuille de propriétés des membres](#members-property-sheet)
-   [Gestion par feuille de propriétés](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Feuille de propriétés général

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **générales** .



| Étiquette d’interface utilisateur                      | Attribut dans Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| nom du groupe (pré-Windows 2000) | [**Nom de compte SAM**](/windows/desktop/ADSchema/a-samaccountname) |
| Description                   | [**Description**](/windows/desktop/ADSchema/a-description)         |
| Courrier électronique                        | [**Adresses de messagerie**](/windows/desktop/ADSchema/a-mail)           |
| Étendue du groupe                   | [**Type de groupe**](/windows/desktop/ADSchema/a-grouptype)            |
| Type de groupe                    | [**Type de groupe**](/windows/desktop/ADSchema/a-grouptype)            |
| Remarques                         | [**Commentaire**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Membre de la feuille de propriétés

Le tableau suivant présente les étiquettes de l’interface utilisateur du **membre de** la feuille de propriétés.



| Étiquette d’interface utilisateur  | Attribut dans Active Directory Domain Services | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membre de | [**Is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contient les noms uniques des groupes auxquels appartient ce groupe. L’attribut de membre de chacun des groupes de cette liste contient le nom unique de cet objet de groupe. L’interface utilisateur ne modifie pas directement l’attribut [**is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof) . Elle modifie l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) sur l’objet de groupe dont cet objet est membre. Le serveur Active Directory gère l’attribut **is-Member-of-DL** .<br/> |



 

## <a name="members-property-sheet"></a>Feuille de propriétés des membres

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés des **membres** .



| Étiquette d’interface utilisateur | Attribut dans Active Directory Domain Services | Description                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Membres  | [**Membre**](/windows/desktop/ADSchema/a-member)               | Contient les noms uniques des membres de cet objet de groupe. |



 

## <a name="managed-by-property-sheet"></a>Gestion par feuille de propriétés

Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **géré par** .



| Étiquette d’interface utilisateur                           | Attribut dans Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nom                               | [**Géré par**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Le gestionnaire peut mettre à jour la liste des membres | Aucun. Une entrée du contrôle d’accès avec l’autorisation « autoriser-écrire des membres » est ajoutée au compte identifié par **nom**.                        |
| Office                             | attribut [**physique-delivery-Office-name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) du compte identifié par **Name**. |
| Rue                             | L’attribut [**rue-adresse**](/windows/desktop/ADSchema/a-street) du compte identifié par le **nom**.                                    |
| City                               | Attribut de [**nom de localité**](/windows/desktop/ADSchema/a-l) du compte identifié par le **nom**.                                          |
| État/Province                     | Attribut [**State-or-province-Name**](/windows/desktop/ADSchema/a-st) du compte identifié par **nom**.                                |
| Pays/région                     | Attribut [**Country-Name**](/windows/desktop/ADSchema/a-c) du compte identifié par **Name**.                                           |
| Numéro de téléphone                   | Attribut de [**numéro de téléphone**](/windows/desktop/ADSchema/a-telephonenumber) du compte identifié par le **nom**.                         |
| Numéro de télécopie                         | Attribut [**télécopie-numéro de téléphone**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) du compte identifié par le **nom**.      |



 

 

