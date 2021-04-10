---
title: Protection des objets contre les effets des droits hérités
description: Comme indiqué dans la rubrique héritage et délégation de l’administration, les ACE peuvent être définies sur un objet conteneur, par exemple organizationalUnit, domainDNS, Container, etc., et propagées aux objets enfants en fonction des indicateurs ACE définis sur ces ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protection des objets des droits hérités AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030993"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>Protection des objets contre les effets des droits hérités

Comme indiqué dans la rubrique [héritage et délégation de l’administration](inheritance-and-delegation-of-administration.md), les ACE peuvent être définies sur un objet conteneur, par **exemple OrganizationalUnit**, **domainDNS**, **Container**, etc., et propagées aux objets enfants en fonction des indicateurs ACE définis sur ces ACE.

Si vous disposez d’un objet sécurisé ou d’un objet dont vous souhaitez contrôler explicitement les ACE, par exemple une unité d’organisation privée ou un utilisateur spécial, vous pouvez empêcher les ACE d’être propagées à l’objet par son conteneur parent ou ses prédécesseurs du conteneur parent.

Utilisez la propriété [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour contrôler si les listes DACL et les listes SACL sont héritées par l’objet de son conteneur parent.

La propriété [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) peut être utilisée pour protéger un objet des effets des ACE héritées. Les indicateurs suivants forcent le contrôle d’accès à être défini explicitement sur l’objet et empêchent un utilisateur de modifier le contrôle d’accès à l’objet en définissant les ACE pouvant être héritées sur le conteneur parent de l’objet, ou les prédécesseurs du conteneur parent.



| Indicateur                               | Description                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_liste DACL de se \_ protégée**<br/> | Empêche les ACE définies sur la liste DACL du conteneur parent et tous les objets au-dessus du conteneur parent dans la hiérarchie de répertoires d’être appliqués à la liste DACL de l’objet.<br/> |
| **\_protection SACL de se \_**<br/> | Empêche les ACE définies sur la liste SACL du conteneur parent et tous les objets au-dessus du conteneur parent dans la hiérarchie de répertoires d’être appliqués à la liste SACL d’objets.<br/> |



 

N’oubliez pas que l’indicateur de **\_ \_ présence DACL se** doit être présent pour définir la **\_ liste DACL \_** de se protégée et que la **\_ liste SACL de se \_** présente doit être présente pour définir la **\_ \_ protection SACL de se**.

 

