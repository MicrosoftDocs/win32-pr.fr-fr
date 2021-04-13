---
title: Propriété ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtient ou définit l’URI de ressource dans un objet ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Propriété ResourceURI Windows Remote Management
- Propriété ResourceURI Windows Remote Management, objet ResourceLocator
- Objet ResourceLocator Windows Remote Management, propriété ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465955"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="e8de4-106">ResourceLocator. ResourceURI, propriété</span><span class="sxs-lookup"><span data-stu-id="e8de4-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="e8de4-107">Obtient ou définit l' [*URI de ressource*](windows-remote-management-glossary.md) dans un objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e8de4-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="e8de4-108">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="e8de4-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="e8de4-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e8de4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8de4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8de4-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="e8de4-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e8de4-111">Property value</span></span>

<span data-ttu-id="e8de4-112">Chaîne qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="e8de4-112">A string that identifies the resource.</span></span> <span data-ttu-id="e8de4-113">Lors de la définition de l’URI de ressource pour un objet [**ResourceLocator**](resourcelocator.md) , l’URI doit contenir uniquement le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e8de4-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8de4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e8de4-114">Remarks</span></span>

<span data-ttu-id="e8de4-115">Voici un exemple de chemin d’accès approprié pour [**resourceuri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="e8de4-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="e8de4-116">Le chemin d’accès suivant ne fonctionne pas, car il contient une clé pour une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="e8de4-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="e8de4-117">Utilisez la méthode [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) pour spécifier une instance particulière.</span><span class="sxs-lookup"><span data-stu-id="e8de4-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="e8de4-118">**IWSManResourceLocator :: resourceuri** est la méthode C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="e8de4-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8de4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8de4-119">Requirements</span></span>



| <span data-ttu-id="e8de4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8de4-120">Requirement</span></span> | <span data-ttu-id="e8de4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8de4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8de4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8de4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8de4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8de4-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e8de4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8de4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8de4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8de4-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e8de4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8de4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8de4-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8de4-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8de4-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="e8de4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8de4-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8de4-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8de4-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8de4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8de4-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8de4-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8de4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e8de4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8de4-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8de4-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8de4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8de4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8de4-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="e8de4-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





