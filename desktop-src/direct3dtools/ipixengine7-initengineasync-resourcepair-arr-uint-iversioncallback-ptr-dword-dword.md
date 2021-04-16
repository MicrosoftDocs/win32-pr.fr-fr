---
description: Transmet de manière asynchrone des ressources au moteur, telles que des chaînes pour les messages d’erreur.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7 :: InitEngineAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482632"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="f059b-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7 :: InitEngineAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="f059b-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="f059b-104">Transmet de manière asynchrone des ressources au moteur, telles que des chaînes pour les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f059b-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="f059b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f059b-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f059b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f059b-106">Parameters</span></span>

<span data-ttu-id="f059b-107">*\_ressources count1* </span><span class="sxs-lookup"><span data-stu-id="f059b-107">*count1\_resources* </span></span>  
<span data-ttu-id="f059b-108">Tableau de ressources.</span><span class="sxs-lookup"><span data-stu-id="f059b-108">An array of resources.</span></span>

<span data-ttu-id="f059b-109">*saut* </span><span class="sxs-lookup"><span data-stu-id="f059b-109">*count* </span></span>  
<span data-ttu-id="f059b-110">Nombre de ressources dans les \_ ressources count1</span><span class="sxs-lookup"><span data-stu-id="f059b-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="f059b-111">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="f059b-111">*versionCallback* </span></span>  
<span data-ttu-id="f059b-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="f059b-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f059b-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="f059b-113">*requestCookie* </span></span>  
<span data-ttu-id="f059b-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="f059b-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f059b-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="f059b-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f059b-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f059b-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f059b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f059b-117">Return value</span></span>

<span data-ttu-id="f059b-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f059b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f059b-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f059b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f059b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f059b-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f059b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f059b-121">Header</span></span></p></td><td><span data-ttu-id="f059b-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f059b-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f059b-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f059b-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f059b-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="f059b-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
