---
description: L’éditeur de contrôle d’accès peut inclure une page de propriétés d’audit qui permet à l’utilisateur d’afficher et de modifier les entrées de contrôle d’accès (ACE) dans une liste de contrôle d’accès système (SACL) d’objets. Pour plus d’informations sur les SACL, consultez listes de Access Control (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Page de propriétés d’audit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203757"
---
# <a name="auditing-property-page"></a><span data-ttu-id="875d0-104">Page de propriétés d’audit</span><span class="sxs-lookup"><span data-stu-id="875d0-104">Auditing Property Page</span></span>

<span data-ttu-id="875d0-105">L’éditeur de contrôle d’accès peut inclure une page de propriétés **d’audit** qui permet à l’utilisateur d’afficher et de modifier les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste de contrôle d' [*accès système*](/windows/desktop/SecGloss/s-gly) (SACL) d’un objet.</span><span class="sxs-lookup"><span data-stu-id="875d0-105">The access control editor can include an **Auditing** property page that enables the user to view and edit the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in an object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="875d0-106">Pour plus d’informations sur les SACL, consultez [listes de Access Control](access-control-lists.md) (ACL).</span><span class="sxs-lookup"><span data-stu-id="875d0-106">For more information about SACLs, see [Access Control Lists](access-control-lists.md) (ACLs).</span></span>

<span data-ttu-id="875d0-107">**Pour afficher la page de propriétés audit**</span><span class="sxs-lookup"><span data-stu-id="875d0-107">**To view the Auditing property page**</span></span>

-   <span data-ttu-id="875d0-108">Sur la [page de propriétés sécurité de base](basic-security-property-page.md), cliquez sur **avancé**.</span><span class="sxs-lookup"><span data-stu-id="875d0-108">On the [basic security property page](basic-security-property-page.md), click **Advanced**.</span></span> <span data-ttu-id="875d0-109">La page de propriétés **Auditing** se trouve dans la [feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md).</span><span class="sxs-lookup"><span data-stu-id="875d0-109">The **Auditing** property page is in the [advanced security property sheet](advanced-security-property-sheet.md).</span></span>

<span data-ttu-id="875d0-110">Pour inclure la page de propriétés **d’audit** , définissez les indicateurs **si \_ avancé** et **si \_ modifier les \_ audits** dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="875d0-110">To include the **Auditing** property page, set the **SI\_ADVANCED** and **SI\_EDIT\_AUDITS** flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
