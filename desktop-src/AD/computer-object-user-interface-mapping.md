---
title: Mappage de l’interface utilisateur de l’objet ordinateur
description: Les tableaux suivants répertorient les éléments des feuilles de propriétés de l’objet ordinateur dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999574"
---
# <a name="computer-object-user-interface-mapping"></a>Mappage de l’interface utilisateur de l’objet ordinateur

Les tableaux suivants répertorient les éléments des feuilles de propriétés de l’objet ordinateur dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.

## <a name="general-property-sheet"></a>Feuille de propriétés général

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés **générales** .



| Étiquette d’interface utilisateur                         | Attribut Active Directory Domain Services | Commentaires                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| nom de l’ordinateur (pré-Windows 2000) | sAMAccountName                             |                                                  |
| Nom DNS                         | dNSHostName                                |                                                  |
| Role                             | userAccountControl                         | Bascule un bit dans le masque de bits userAccountControl. |
| Description                      | description                                |                                                  |
| Approuver l’ordinateur pour la délégation    | userAccountControl                         | Bascule un bit dans le masque de bits userAccountControl. |



 

## <a name="location-property-sheet"></a>Feuille de propriétés de l’emplacement

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés d' **emplacement** .



| Étiquette d’interface utilisateur | Attribut Active Directory Domain Services |
|----------|--------------------------------------------|
| Emplacement | location                                   |



 

## <a name="member-of-property-sheet"></a>Membre de la feuille de propriétés

Le tableau suivant répertorie les étiquettes de l’interface utilisateur du **membre de** la feuille de propriétés.



| Étiquette d’interface utilisateur          | Attribut Active Directory Domain Services | Commentaires                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membre de         | memberOf                                   | Comprend tous les groupes de la liste des interfaces utilisateur, à l’exception du groupe principal, qui est représenté dans la publicité via l’attribut [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Définir le groupe principal | primaryGroupID                             | LDAP : lié à [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) du groupe principal.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Feuille de propriétés du système d’exploitation

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés du **système d’exploitation** .



| Étiquette d’interface utilisateur     | Attribut Active Directory Domain Services |
|--------------|--------------------------------------------|
| Nom         | operatingSystem                            |
| Version      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 