---
description: Obtient l’adresse de point de terminaison d’un moteur distant.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPeerToPeerEngine :: GetPlaybackEndpoint, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521143"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="4cfe0-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine :: GetPlaybackEndpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="4cfe0-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="4cfe0-104">Obtient l’adresse de point de terminaison d’un moteur distant.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfe0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cfe0-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="4cfe0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cfe0-106">Parameters</span></span>

<span data-ttu-id="4cfe0-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="4cfe0-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="4cfe0-108">true si le moteur distant utilise l’authentification ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="4cfe0-109">*pEndpoint* </span><span class="sxs-lookup"><span data-stu-id="4cfe0-109">*pEndpoint* </span></span>  
<span data-ttu-id="4cfe0-110">Au retour, chaîne COM contenant l’adresse de point de terminaison de l’ordinateur de lecture à distance.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="4cfe0-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="4cfe0-111">*sessionKey* </span></span>  
<span data-ttu-id="4cfe0-112">Au retour, chaîne COM contenant la clé de session utilisée pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="4cfe0-113">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="4cfe0-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="4cfe0-114">Au retour, version du moteur distant.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="4cfe0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cfe0-115">Return value</span></span>

<span data-ttu-id="4cfe0-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4cfe0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4cfe0-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cfe0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfe0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cfe0-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4cfe0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cfe0-119">Header</span></span></p></td><td><span data-ttu-id="4cfe0-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4cfe0-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4cfe0-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cfe0-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4cfe0-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="4cfe0-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
