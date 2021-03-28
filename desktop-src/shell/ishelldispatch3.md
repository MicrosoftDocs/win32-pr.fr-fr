---
description: Étend l’objet IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objet IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972375"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="54961-103">Objet IShellDispatch3</span><span class="sxs-lookup"><span data-stu-id="54961-103">IShellDispatch3 object</span></span>

<span data-ttu-id="54961-104">Étend l’objet [**IShellDispatch2**](ishelldispatch2-object.md) .</span><span class="sxs-lookup"><span data-stu-id="54961-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="54961-105">**IShellDispatch3** prend en charge une nouvelle méthode en plus des propriétés et des méthodes prises en charge par **IShellDispatch2**.</span><span class="sxs-lookup"><span data-stu-id="54961-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="54961-106">**IShellDispatch3** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="54961-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="54961-107">Membres</span><span class="sxs-lookup"><span data-stu-id="54961-107">Members</span></span>

<span data-ttu-id="54961-108">L’objet **IShellDispatch3** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="54961-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="54961-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54961-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54961-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54961-110">Methods</span></span>

<span data-ttu-id="54961-111">L’objet **IShellDispatch3** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="54961-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="54961-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="54961-112">Method</span></span>                                             | <span data-ttu-id="54961-113">Description</span><span class="sxs-lookup"><span data-stu-id="54961-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="54961-114">**AddToRecent**</span><span class="sxs-lookup"><span data-stu-id="54961-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="54961-115">Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="54961-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54961-116">Notes</span><span class="sxs-lookup"><span data-stu-id="54961-116">Remarks</span></span>

<span data-ttu-id="54961-117">Pour plus d’informations sur les services Windows, consultez la documentation relative aux [services](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="54961-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="54961-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54961-118">Requirements</span></span>



| <span data-ttu-id="54961-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54961-119">Requirement</span></span> | <span data-ttu-id="54961-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="54961-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54961-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54961-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54961-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54961-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="54961-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54961-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54961-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54961-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54961-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="54961-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="54961-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54961-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="54961-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="54961-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54961-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54961-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="54961-129">DLL</span><span class="sxs-lookup"><span data-stu-id="54961-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54961-130"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="54961-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54961-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54961-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54961-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="54961-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="54961-133">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="54961-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="54961-134">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="54961-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="54961-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="54961-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
