---
description: Définit de manière asynchrone l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7 :: SetPlaybackEndpointAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747388"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="6cd17-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7 :: SetPlaybackEndpointAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="6cd17-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="6cd17-104">Définit de manière asynchrone l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.</span><span class="sxs-lookup"><span data-stu-id="6cd17-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cd17-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="6cd17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cd17-106">Parameters</span></span>

<span data-ttu-id="6cd17-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="6cd17-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="6cd17-108">true pour utiliser l’authentification ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="6cd17-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="6cd17-109">*poste* </span><span class="sxs-lookup"><span data-stu-id="6cd17-109">*endpoint* </span></span>  
<span data-ttu-id="6cd17-110">Chaîne COM contenant l’adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6cd17-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="6cd17-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="6cd17-111">*sessionKey* </span></span>  
<span data-ttu-id="6cd17-112">Chaîne COM contenant la clé de session utilisée pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="6cd17-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="6cd17-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="6cd17-113">*remoteVersion* </span></span>  
<span data-ttu-id="6cd17-114">Spécifie la version du moteur distant à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6cd17-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="6cd17-115">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="6cd17-115">*versionCallback* </span></span>  
<span data-ttu-id="6cd17-116">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="6cd17-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="6cd17-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="6cd17-117">*requestCookie* </span></span>  
<span data-ttu-id="6cd17-118">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="6cd17-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="6cd17-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="6cd17-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="6cd17-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6cd17-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cd17-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cd17-121">Return value</span></span>

<span data-ttu-id="6cd17-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6cd17-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6cd17-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cd17-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd17-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cd17-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6cd17-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cd17-125">Header</span></span></p></td><td><span data-ttu-id="6cd17-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6cd17-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6cd17-127"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cd17-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6cd17-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="6cd17-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
