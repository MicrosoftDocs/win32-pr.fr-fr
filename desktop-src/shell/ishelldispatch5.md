---
description: Étend l’objet IShellDispatch4.
title: Objet IShellDispatch5 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972355"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="71c9c-103">Objet IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="71c9c-103">IShellDispatch5 object</span></span>

<span data-ttu-id="71c9c-104">Étend l’objet [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="71c9c-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="71c9c-105">En plus des propriétés et des méthodes prises en charge par **IShellDispatch4**, **IShellDispatch5** ajoute une méthode qui affiche les fenêtres ouvertes dans une pile 3D.</span><span class="sxs-lookup"><span data-stu-id="71c9c-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="71c9c-106">**IShellDispatch5** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="71c9c-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="71c9c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="71c9c-107">Members</span></span>

<span data-ttu-id="71c9c-108">L’objet **IShellDispatch5** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71c9c-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="71c9c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71c9c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="71c9c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71c9c-110">Methods</span></span>

<span data-ttu-id="71c9c-111">L’objet **IShellDispatch5** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="71c9c-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="71c9c-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="71c9c-112">Method</span></span>                                                   | <span data-ttu-id="71c9c-113">Description</span><span class="sxs-lookup"><span data-stu-id="71c9c-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="71c9c-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="71c9c-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="71c9c-115">Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.</span><span class="sxs-lookup"><span data-stu-id="71c9c-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71c9c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71c9c-116">Requirements</span></span>



| <span data-ttu-id="71c9c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c9c-117">Requirement</span></span> | <span data-ttu-id="71c9c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c9c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c9c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71c9c-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c9c-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="71c9c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71c9c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c9c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71c9c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="71c9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71c9c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="71c9c-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="71c9c-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="71c9c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71c9c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71c9c-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="71c9c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="71c9c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c9c-128"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="71c9c-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c9c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71c9c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c9c-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="71c9c-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="71c9c-131">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="71c9c-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="71c9c-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="71c9c-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="71c9c-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="71c9c-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="71c9c-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="71c9c-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="71c9c-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="71c9c-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
