---
description: La feuille de propriétés de sécurité avancée permet à l’utilisateur d’effectuer des opérations de modification qui ne sont pas disponibles sur la page de propriétés sécurité de base d’un éditeur de contrôle d’accès.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Feuille de propriétés de sécurité avancée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545157"
---
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="f8ee7-103">Feuille de propriétés de sécurité avancée</span><span class="sxs-lookup"><span data-stu-id="f8ee7-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="f8ee7-104">La feuille de propriétés de sécurité avancée permet à l’utilisateur d’effectuer des opérations de modification qui ne sont pas disponibles sur la [page de propriétés sécurité de base](basic-security-property-page.md) d’un éditeur de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="f8ee7-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="f8ee7-105">La feuille de propriétés peut inclure les pages de propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8ee7-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="f8ee7-106">Une page de propriétés des [autorisations](permissions-property-page.md) pour la modification avancée de la liste de contrôle d’accès discrétionnaire de l’objet (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ), telle que la modification des [ACE spécifiques à un objet ou le](object-specific-aces.md) contrôle de [l’héritage d’ACE](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="f8ee7-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="f8ee7-107">Une page de propriétés [d’audit](auditing-property-page.md) pour l’affichage et la modification de la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8ee7-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="f8ee7-108">Page de propriétés [propriétaire](owner-property-page.md) permettant de modifier le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f8ee7-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="f8ee7-109">L’utilisateur peut afficher la feuille de propriétés de sécurité avancée en cliquant sur le bouton **avancé** de la page de propriétés sécurité de base.</span><span class="sxs-lookup"><span data-stu-id="f8ee7-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="f8ee7-110">Pour afficher le bouton **avancé** , définissez l' \_ indicateur si avancé dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="f8ee7-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
