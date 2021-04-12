---
description: Transmet des ressources au moteur, telles que des chaînes pour les messages d’erreur.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine3 :: SetupResources, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109319"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span data-ttu-id="00409-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3 :: SetupResources, méthode</span><span class="sxs-lookup"><span data-stu-id="00409-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources method</span></span>

<span data-ttu-id="00409-104">Transmet des ressources au moteur, telles que des chaînes pour les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="00409-104">Passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="00409-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00409-105">Syntax</span></span>


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a><span data-ttu-id="00409-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00409-106">Parameters</span></span>

<span data-ttu-id="00409-107">*\_ressources count1* </span><span class="sxs-lookup"><span data-stu-id="00409-107">*count1\_resources* </span></span>  
<span data-ttu-id="00409-108">Ressources de ressources passées.</span><span class="sxs-lookup"><span data-stu-id="00409-108">The resources resources passed.</span></span>

<span data-ttu-id="00409-109">*saut* </span><span class="sxs-lookup"><span data-stu-id="00409-109">*count* </span></span>  
<span data-ttu-id="00409-110">Nombre de ressources passées.</span><span class="sxs-lookup"><span data-stu-id="00409-110">The number of resources passed.</span></span>

## <a name="return-value"></a><span data-ttu-id="00409-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00409-111">Return value</span></span>

<span data-ttu-id="00409-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="00409-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00409-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00409-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="00409-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00409-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="00409-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="00409-115">Header</span></span></p></td><td><span data-ttu-id="00409-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="00409-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="00409-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00409-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="00409-118">**IPixEngine3**</span><span class="sxs-lookup"><span data-stu-id="00409-118">**IPixEngine3**</span></span>](/windows/desktop/direct3dtools/ipixengine3)

 

 
