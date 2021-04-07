---
title: Access Control et suppression d’objets
description: Active Directory vous permet de supprimer un objet si vous avez la possibilité de supprimer l’accès à l’objet ou aux publicités \_ droit \_ DS \_ supprimer \_ l’accès enfant au type d’objet sur le conteneur parent.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD Access Control et suppression d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724373"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="4a62b-104">Access Control et suppression d’objets</span><span class="sxs-lookup"><span data-stu-id="4a62b-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="4a62b-105">Active Directory Domain Services vous permettent de supprimer un objet si vous disposez de l’un des droits d’accès suivants :</span><span class="sxs-lookup"><span data-stu-id="4a62b-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="4a62b-106">SUPPRIMER l’accès à l’objet lui-même</span><span class="sxs-lookup"><span data-stu-id="4a62b-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="4a62b-107">AD \_ Right \_ DS \_ Supprimer l' \_ accès enfant pour ce type d’objet sur le conteneur parent</span><span class="sxs-lookup"><span data-stu-id="4a62b-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="4a62b-108">N’oubliez pas que le système vérifie le descripteur de sécurité pour l’objet et son parent avant de refuser la suppression.</span><span class="sxs-lookup"><span data-stu-id="4a62b-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="4a62b-109">Cela signifie qu’une entrée du contrôle d’accès qui refuse explicitement l’accès en suppression à un utilisateur n’a aucun effet si l’utilisateur a supprimé l' \_ accès enfant sur le parent.</span><span class="sxs-lookup"><span data-stu-id="4a62b-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="4a62b-110">De même, une entrée du contrôle d’accès qui refuse l' \_ accès à la suppression d’un enfant sur le parent peut être remplacée si l’accès en suppression est autorisé sur l’objet lui-même.</span><span class="sxs-lookup"><span data-stu-id="4a62b-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="4a62b-111">Pour effectuer une opération de suppression d’arborescence, par exemple à l’aide de la méthode [**IADsDeleteOps ::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , vous devez disposer des \_ services de domaine Active \_ Directory droit supprimer l' \_ \_ accès à l’arborescence pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="4a62b-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="4a62b-112">Si vous disposez de ce droit d’accès, vous pouvez supprimer l’objet et tous les objets enfants, quelles que soient les protections sur les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="4a62b-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="4a62b-113">Pour supprimer une arborescence si vous n’avez pas d' \_ \_ accès à la suppression de l’arborescence des services de domaine Active Directory \_ \_ , vous devez parcourir de manière récursive l’arborescence, en supprimant chaque objet individuellement.</span><span class="sxs-lookup"><span data-stu-id="4a62b-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="4a62b-114">Dans ce cas, vous devez disposer de l’accès de suppression ou de suppression \_ d’enfant nécessaire pour chaque objet de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="4a62b-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="4a62b-115">Si les utilisateurs disposent d’un \_ droit de \_ Suppression d’arborescence des services de domaine Active Directory \_ \_ pour un objet, ils peuvent supprimer l’intégralité d’une sous-arborescence, y compris tous les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="4a62b-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="4a62b-116">Pour cette raison, vous pouvez envisager de révoquer l’autorisation d’accès « supprimer la sous-arborescence » pour tous les utilisateurs sur un conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="4a62b-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 