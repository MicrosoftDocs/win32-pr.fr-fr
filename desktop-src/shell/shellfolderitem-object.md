---
description: Étend l’objet FolderItem. En plus des propriétés et des méthodes prises en charge par FolderItem, ShellFolderItem a deux méthodes supplémentaires.
title: Objet ShellFolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840770"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="14543-104">Objet ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="14543-104">ShellFolderItem object</span></span>

<span data-ttu-id="14543-105">Étend l’objet [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="14543-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="14543-106">En plus des propriétés et des méthodes prises en charge par **FolderItem**, **ShellFolderItem** a deux méthodes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="14543-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="14543-107">Membres</span><span class="sxs-lookup"><span data-stu-id="14543-107">Members</span></span>

<span data-ttu-id="14543-108">L’objet **ShellFolderItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="14543-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="14543-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14543-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14543-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="14543-110">Methods</span></span>

<span data-ttu-id="14543-111">L’objet **ShellFolderItem** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="14543-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="14543-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="14543-112">Method</span></span>                                                       | <span data-ttu-id="14543-113">Description</span><span class="sxs-lookup"><span data-stu-id="14543-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14543-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="14543-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="14543-115">Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="14543-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="14543-116">La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="14543-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="14543-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="14543-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="14543-118">Exécute un verbe sur un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="14543-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="14543-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="14543-119">Requirements</span></span>



| <span data-ttu-id="14543-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14543-120">Requirement</span></span> | <span data-ttu-id="14543-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="14543-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14543-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14543-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14543-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14543-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14543-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14543-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14543-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14543-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="14543-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="14543-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14543-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14543-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="14543-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="14543-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14543-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14543-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="14543-130">DLL</span><span class="sxs-lookup"><span data-stu-id="14543-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14543-131"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="14543-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




