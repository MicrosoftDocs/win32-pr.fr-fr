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
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="52d36-104">Protection des objets contre les effets des droits hérités</span><span class="sxs-lookup"><span data-stu-id="52d36-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="52d36-105">Comme indiqué dans la rubrique [héritage et délégation de l’administration](inheritance-and-delegation-of-administration.md), les ACE peuvent être définies sur un objet conteneur, par **exemple OrganizationalUnit**, **domainDNS**, **Container**, etc., et propagées aux objets enfants en fonction des indicateurs ACE définis sur ces ACE.</span><span class="sxs-lookup"><span data-stu-id="52d36-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="52d36-106">Si vous disposez d’un objet sécurisé ou d’un objet dont vous souhaitez contrôler explicitement les ACE, par exemple une unité d’organisation privée ou un utilisateur spécial, vous pouvez empêcher les ACE d’être propagées à l’objet par son conteneur parent ou ses prédécesseurs du conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="52d36-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="52d36-107">Utilisez la propriété [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour contrôler si les listes DACL et les listes SACL sont héritées par l’objet de son conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="52d36-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="52d36-108">La propriété [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) peut être utilisée pour protéger un objet des effets des ACE héritées.</span><span class="sxs-lookup"><span data-stu-id="52d36-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="52d36-109">Les indicateurs suivants forcent le contrôle d’accès à être défini explicitement sur l’objet et empêchent un utilisateur de modifier le contrôle d’accès à l’objet en définissant les ACE pouvant être héritées sur le conteneur parent de l’objet, ou les prédécesseurs du conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="52d36-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="52d36-110">Indicateur</span><span class="sxs-lookup"><span data-stu-id="52d36-110">Flag</span></span>                               | <span data-ttu-id="52d36-111">Description</span><span class="sxs-lookup"><span data-stu-id="52d36-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d36-112">**\_liste DACL de se \_ protégée**</span><span class="sxs-lookup"><span data-stu-id="52d36-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="52d36-113">Empêche les ACE définies sur la liste DACL du conteneur parent et tous les objets au-dessus du conteneur parent dans la hiérarchie de répertoires d’être appliqués à la liste DACL de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52d36-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="52d36-114">**\_protection SACL de se \_**</span><span class="sxs-lookup"><span data-stu-id="52d36-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="52d36-115">Empêche les ACE définies sur la liste SACL du conteneur parent et tous les objets au-dessus du conteneur parent dans la hiérarchie de répertoires d’être appliqués à la liste SACL d’objets.</span><span class="sxs-lookup"><span data-stu-id="52d36-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="52d36-116">N’oubliez pas que l’indicateur de **\_ \_ présence DACL se** doit être présent pour définir la **\_ liste DACL \_** de se protégée et que la **\_ liste SACL de se \_** présente doit être présente pour définir la **\_ \_ protection SACL de se**.</span><span class="sxs-lookup"><span data-stu-id="52d36-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 

