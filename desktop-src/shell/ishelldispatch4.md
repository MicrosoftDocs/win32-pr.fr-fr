---
description: Étend l’objet IShellDispatch3.
title: Objet IShellDispatch4 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843060"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="ca6fb-103">Objet IShellDispatch4</span><span class="sxs-lookup"><span data-stu-id="ca6fb-103">IShellDispatch4 object</span></span>

<span data-ttu-id="ca6fb-104">Étend l’objet [**IShellDispatch3**](ishelldispatch3.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6fb-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="ca6fb-105">Outre les propriétés et les méthodes prises en charge par **IShellDispatch3**, **IShellDispatch4** prend en charge quatre méthodes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="ca6fb-106">**IShellDispatch4** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6fb-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ca6fb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ca6fb-107">Members</span></span>

<span data-ttu-id="ca6fb-108">L’objet **IShellDispatch4** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ca6fb-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="ca6fb-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ca6fb-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ca6fb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ca6fb-110">Methods</span></span>

<span data-ttu-id="ca6fb-111">L’objet **IShellDispatch4** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="ca6fb-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="ca6fb-112">Method</span></span>                                                     | <span data-ttu-id="ca6fb-113">Description</span><span class="sxs-lookup"><span data-stu-id="ca6fb-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="ca6fb-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="ca6fb-115">Obtient la valeur d’une stratégie Internet Explorer spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="ca6fb-116">**GetSetting**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="ca6fb-117">Récupère un paramètre d’interpréteur de commandes global.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="ca6fb-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="ca6fb-119">Affiche ou masque le bureau.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="ca6fb-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="ca6fb-121">Affiche la boîte de dialogue **sécurité Windows** .</span><span class="sxs-lookup"><span data-stu-id="ca6fb-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="ca6fb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ca6fb-122">Remarks</span></span>

<span data-ttu-id="ca6fb-123">Pour plus d’informations sur les services Windows, consultez la documentation relative aux [services](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6fb-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6fb-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca6fb-124">Requirements</span></span>



| <span data-ttu-id="ca6fb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca6fb-125">Requirement</span></span> | <span data-ttu-id="ca6fb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca6fb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6fb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca6fb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6fb-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca6fb-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ca6fb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca6fb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6fb-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca6fb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ca6fb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca6fb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6fb-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca6fb-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ca6fb-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="ca6fb-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca6fb-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca6fb-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ca6fb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ca6fb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca6fb-136"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ca6fb-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca6fb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca6fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6fb-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ca6fb-139">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="ca6fb-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="ca6fb-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="ca6fb-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="ca6fb-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
