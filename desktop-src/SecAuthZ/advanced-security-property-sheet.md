---
description: La feuille de propriétés de sécurité avancée permet à l’utilisateur d’effectuer des opérations de modification qui ne sont pas disponibles sur la page de propriétés sécurité de base d’un éditeur de contrôle d’accès.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Feuille de propriétés de sécurité avancée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013719"
---
# <a name="advanced-security-property-sheet"></a>Feuille de propriétés de sécurité avancée

La feuille de propriétés de sécurité avancée permet à l’utilisateur d’effectuer des opérations de modification qui ne sont pas disponibles sur la [page de propriétés sécurité de base](basic-security-property-page.md) d’un éditeur de contrôle d’accès. La feuille de propriétés peut inclure les pages de propriétés suivantes :

-   Une page de propriétés des [autorisations](permissions-property-page.md) pour la modification avancée de la liste de contrôle d’accès discrétionnaire de l’objet (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ), telle que la modification des [ACE spécifiques à un objet ou le](object-specific-aces.md) contrôle de [l’héritage d’ACE](ace-inheritance.md).
-   Une page de propriétés [d’audit](auditing-property-page.md) pour l’affichage et la modification de la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) de l’objet.
-   Page de propriétés [propriétaire](owner-property-page.md) permettant de modifier le propriétaire de l’objet.

L’utilisateur peut afficher la feuille de propriétés de sécurité avancée en cliquant sur le bouton **avancé** de la page de propriétés sécurité de base. Pour afficher le bouton **avancé** , définissez l' \_ indicateur si avancé dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
