---
description: Étend l’objet IShellDispatch5.
title: Objet IShellDispatch6 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: 42e9690ec5b2f5995b184e4e686b27037aab891d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113971"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="51252-103">Objet IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="51252-103">IShellDispatch6 object</span></span>

<span data-ttu-id="51252-104">Étend l’objet [**IShellDispatch5**](ishelldispatch5.md) .</span><span class="sxs-lookup"><span data-stu-id="51252-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="51252-105">En plus des propriétés et des méthodes prises en charge par **IShellDispatch5**, **IShellDispatch6** ajoute une méthode qui affiche le volet de recherche applications.</span><span class="sxs-lookup"><span data-stu-id="51252-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="51252-106">**IShellDispatch6** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="51252-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="51252-107">Membres</span><span class="sxs-lookup"><span data-stu-id="51252-107">Members</span></span>

<span data-ttu-id="51252-108">L’objet **IShellDispatch6** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="51252-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="51252-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="51252-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="51252-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="51252-110">Methods</span></span>

<span data-ttu-id="51252-111">L’objet **IShellDispatch6** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="51252-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="51252-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="51252-112">Method</span></span>                                                 | <span data-ttu-id="51252-113">Description</span><span class="sxs-lookup"><span data-stu-id="51252-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51252-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="51252-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="51252-115">Affiche le volet de recherche applications, qui apparaît normalement lorsque vous commencez à taper un terme de recherche à partir de l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="51252-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51252-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="51252-116">Requirements</span></span>



| <span data-ttu-id="51252-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51252-117">Requirement</span></span> | <span data-ttu-id="51252-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="51252-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51252-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51252-119">Minimum supported client</span></span><br/> | <span data-ttu-id="51252-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51252-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51252-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51252-121">Minimum supported server</span></span><br/> | <span data-ttu-id="51252-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51252-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51252-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="51252-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51252-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51252-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="51252-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="51252-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51252-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51252-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="51252-127">DLL</span><span class="sxs-lookup"><span data-stu-id="51252-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51252-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51252-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51252-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51252-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51252-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="51252-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="51252-131">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="51252-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="51252-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="51252-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="51252-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="51252-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="51252-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="51252-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="51252-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="51252-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="51252-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="51252-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
