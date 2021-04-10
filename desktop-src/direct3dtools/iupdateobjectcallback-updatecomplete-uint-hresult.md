---
description: Rappel utilisé pour notifier l’hôte qu’un objet a été mis à jour.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IUpdateObjectCallback :: UpdateComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109298"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="35269-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback :: UpdateComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="35269-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="35269-104">Rappel utilisé pour notifier l’hôte qu’un objet a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="35269-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="35269-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35269-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="35269-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35269-106">Parameters</span></span>

<span data-ttu-id="35269-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="35269-107">*objectAddress* </span></span>  
<span data-ttu-id="35269-108">ID de l’objet qui a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="35269-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="35269-109">*venir* </span><span class="sxs-lookup"><span data-stu-id="35269-109">*result* </span></span>  
<span data-ttu-id="35269-110">Indique si la mise à jour a réussi.</span><span class="sxs-lookup"><span data-stu-id="35269-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="35269-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35269-111">Return value</span></span>

<span data-ttu-id="35269-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="35269-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35269-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35269-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="35269-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35269-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="35269-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="35269-115">Header</span></span></p></td><td><span data-ttu-id="35269-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="35269-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="35269-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35269-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="35269-118">**IUpdateObjectCallback**</span><span class="sxs-lookup"><span data-stu-id="35269-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
