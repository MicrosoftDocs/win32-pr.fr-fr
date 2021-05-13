---
description: Étend l’objet FolderItems. Il prend en charge une méthode supplémentaire.
title: Objet FolderItems2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0ca0efb3-6831-4561-9fd1-6d0b62704931
ms.openlocfilehash: b11bc4d1b3cd2bdd71802e79ca959c0a0f84e360
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840970"
---
# <a name="folderitems2-object"></a><span data-ttu-id="4e051-104">Objet FolderItems2</span><span class="sxs-lookup"><span data-stu-id="4e051-104">FolderItems2 object</span></span>

<span data-ttu-id="4e051-105">Étend l’objet [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="4e051-105">Extends the [**FolderItems**](folderitems.md) object.</span></span> <span data-ttu-id="4e051-106">Il prend en charge une méthode supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4e051-106">It supports one additional method.</span></span>

## <a name="members"></a><span data-ttu-id="4e051-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4e051-107">Members</span></span>

<span data-ttu-id="4e051-108">L’objet **FolderItems2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4e051-108">The **FolderItems2** object has these types of members:</span></span>

-   [<span data-ttu-id="4e051-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e051-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e051-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e051-110">Methods</span></span>

<span data-ttu-id="4e051-111">L’objet **FolderItems2** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e051-111">The **FolderItems2** object has these methods.</span></span>



| <span data-ttu-id="4e051-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="4e051-112">Method</span></span>                                            | <span data-ttu-id="4e051-113">Description</span><span class="sxs-lookup"><span data-stu-id="4e051-113">Description</span></span>                                                                                                                                                                                                                                         |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e051-114">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="4e051-114">**InvokeVerbEx**</span></span>](folderitems2-invokeverbex.md) | <span data-ttu-id="4e051-115">Exécute un verbe sur une collection d’objets [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4e051-115">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="4e051-116">Cette méthode est une extension de la méthode [**InvokeVerb**](folderitem-invokeverb.md) , qui permet un contrôle supplémentaire de l’opération via un ensemble d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4e051-116">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4e051-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4e051-117">Requirements</span></span>



| <span data-ttu-id="4e051-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e051-118">Requirement</span></span> | <span data-ttu-id="4e051-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e051-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e051-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e051-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e051-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e051-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e051-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e051-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e051-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e051-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e051-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e051-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e051-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e051-125"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4e051-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="4e051-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e051-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e051-127"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4e051-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4e051-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e051-129"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4e051-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e051-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e051-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e051-131">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="4e051-131">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="4e051-132">**ShellExecuteEx**</span><span class="sxs-lookup"><span data-stu-id="4e051-132">**ShellExecuteEx**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)
</dt> </dl>

 

 




