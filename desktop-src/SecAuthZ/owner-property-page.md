---
description: L’éditeur de contrôle d’accès peut inclure une page de propriétés de propriétaire qui permet à l’utilisateur de modifier un propriétaire d’objets. Pour plus d’informations sur le propriétaire d’objets, consultez propriétaire d’un nouvel objet et appropriation d’objets en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Page de propriétés propriétaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115814"
---
# <a name="owner-property-page"></a><span data-ttu-id="7f957-104">Page de propriétés propriétaire</span><span class="sxs-lookup"><span data-stu-id="7f957-104">Owner Property Page</span></span>

<span data-ttu-id="7f957-105">L’éditeur de contrôle d’accès peut inclure une page de propriétés de propriétaire qui permet à l’utilisateur de modifier le propriétaire d’un objet.</span><span class="sxs-lookup"><span data-stu-id="7f957-105">The access control editor can include an Owner property page that enables the user to change an object's owner.</span></span> <span data-ttu-id="7f957-106">Pour plus d’informations sur le propriétaire d’un objet, consultez [propriétaire d’un nouvel objet](owner-of-a-new-object.md) et [appropriation d’objets en C++](taking-object-ownership-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7f957-106">For more information about an object's owner, see [Owner of a New Object](owner-of-a-new-object.md) and [Taking Object Ownership in C++](taking-object-ownership-in-c--.md).</span></span>

<span data-ttu-id="7f957-107">La page de propriétés **propriétaire** se trouve dans la [feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md) qui s’affiche lorsque l’utilisateur clique sur le bouton **avancé** de la [page de propriétés sécurité de base](basic-security-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="7f957-107">The **Owner** property page is in the [advanced security property sheet](advanced-security-property-sheet.md) displayed when the user clicks the **Advanced** button on the [basic security property page](basic-security-property-page.md).</span></span> <span data-ttu-id="7f957-108">Pour inclure la page de propriétés **propriétaire** , définissez les \_ indicateurs SI avancé et si \_ modifier \_ le propriétaire dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="7f957-108">To include the **Owner** property page, set the SI\_ADVANCED and SI\_EDIT\_OWNER flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
