---
description: Connectez-vous à une autre instance d’un moteur distant sur l’ordinateur local.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IServerConnectionCallback :: ConnectToEngine, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109739"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="f3d0d-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback :: ConnectToEngine, méthode</span><span class="sxs-lookup"><span data-stu-id="f3d0d-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="f3d0d-104">Connectez-vous à une autre instance d’un moteur distant sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f3d0d-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3d0d-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="f3d0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3d0d-106">Parameters</span></span>

<span data-ttu-id="f3d0d-107">*bLegacyConnection* </span><span class="sxs-lookup"><span data-stu-id="f3d0d-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="f3d0d-108">true si le moteur utilise est hérité, sinon false.</span><span class="sxs-lookup"><span data-stu-id="f3d0d-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="f3d0d-109">*runAddress* </span><span class="sxs-lookup"><span data-stu-id="f3d0d-109">*runAddress* </span></span>  
<span data-ttu-id="f3d0d-110">Chaîne COM contenant le nom de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f3d0d-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="f3d0d-111">*ppEngineCreated* </span><span class="sxs-lookup"><span data-stu-id="f3d0d-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="f3d0d-112">Au retour, adresse de l’instance du moteur.</span><span class="sxs-lookup"><span data-stu-id="f3d0d-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3d0d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3d0d-113">Return value</span></span>

<span data-ttu-id="f3d0d-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f3d0d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3d0d-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3d0d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d0d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3d0d-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3d0d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3d0d-117">Header</span></span></p></td><td><span data-ttu-id="f3d0d-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f3d0d-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f3d0d-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3d0d-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f3d0d-120">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="f3d0d-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
