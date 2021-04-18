---
description: Demande asynchrone d’obtenir des données de maillage à partir de l’événement spécifié.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest3 :: RequestMeshAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519180"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="3a999-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3 :: RequestMeshAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="3a999-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="3a999-104">Demande asynchrone d’obtenir des données de maillage à partir de l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a999-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a999-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a999-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3a999-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a999-106">Parameters</span></span>

<span data-ttu-id="3a999-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="3a999-107">*eventID* </span></span>  
<span data-ttu-id="3a999-108">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a999-108">The specified event.</span></span>

<span data-ttu-id="3a999-109">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="3a999-109">*meshFilename* </span></span>  
<span data-ttu-id="3a999-110">Chaîne COM contenant le nom du chemin d’accès du fichier dans lequel les données de maillage sont écrites.</span><span class="sxs-lookup"><span data-stu-id="3a999-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="3a999-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="3a999-111">*requestCallback* </span></span>  
<span data-ttu-id="3a999-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="3a999-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="3a999-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="3a999-113">*requestCookie* </span></span>  
<span data-ttu-id="3a999-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="3a999-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3a999-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="3a999-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3a999-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3a999-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a999-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a999-117">Return value</span></span>

<span data-ttu-id="3a999-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a999-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a999-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a999-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a999-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a999-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3a999-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a999-121">Header</span></span></p></td><td><span data-ttu-id="3a999-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3a999-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3a999-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a999-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3a999-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="3a999-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
