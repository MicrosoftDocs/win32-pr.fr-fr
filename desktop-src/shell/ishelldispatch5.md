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
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843000"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="17911-103">Objet IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="17911-103">IShellDispatch5 object</span></span>

<span data-ttu-id="17911-104">Étend l’objet [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="17911-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="17911-105">En plus des propriétés et des méthodes prises en charge par **IShellDispatch4**, **IShellDispatch5** ajoute une méthode qui affiche les fenêtres ouvertes dans une pile 3D.</span><span class="sxs-lookup"><span data-stu-id="17911-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="17911-106">**IShellDispatch5** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="17911-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="17911-107">Membres</span><span class="sxs-lookup"><span data-stu-id="17911-107">Members</span></span>

<span data-ttu-id="17911-108">L’objet **IShellDispatch5** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17911-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="17911-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17911-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17911-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17911-110">Methods</span></span>

<span data-ttu-id="17911-111">L’objet **IShellDispatch5** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="17911-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="17911-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="17911-112">Method</span></span>                                                   | <span data-ttu-id="17911-113">Description</span><span class="sxs-lookup"><span data-stu-id="17911-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="17911-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="17911-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="17911-115">Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.</span><span class="sxs-lookup"><span data-stu-id="17911-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17911-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="17911-116">Requirements</span></span>



| <span data-ttu-id="17911-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17911-117">Requirement</span></span> | <span data-ttu-id="17911-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="17911-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17911-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17911-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17911-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17911-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="17911-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17911-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17911-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17911-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17911-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="17911-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17911-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17911-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="17911-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="17911-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17911-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17911-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="17911-127">DLL</span><span class="sxs-lookup"><span data-stu-id="17911-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17911-128"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="17911-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17911-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17911-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17911-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="17911-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="17911-131">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="17911-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="17911-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="17911-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="17911-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="17911-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="17911-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="17911-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="17911-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="17911-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
