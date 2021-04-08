---
description: Demandez un jeton pour le point de terminaison du service à l’aide des informations d’identification spécifiées.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider :: GetEndpointToken, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752077"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="0ce3f-103">IUpdateEndpointAuthProvider :: GetEndpointToken, méthode</span><span class="sxs-lookup"><span data-stu-id="0ce3f-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="0ce3f-104">Demandez un jeton pour le point de terminaison du service à l’aide des informations d’identification spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ce3f-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="0ce3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ce3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce3f-107">*ServiceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-108">Identifie le service à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3f-109">*endpointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-110">Identifie le type de point de terminaison implémenté par le service.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3f-111">*proxySettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-112">Paramètres à utiliser lors de la connexion à un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="0ce3f-113">Pour plus d’informations, consultez la structure [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce3f-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3f-114">*hUserToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0ce3f-115">*TokenType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-116">Identifie le type de jeton d’authentification utilisé pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3f-117">*fRefreshOnline* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-118">Indique que Weather WUA demande un nouveau jeton.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="0ce3f-119">La valeur true indique qu’un nouveau jeton est demandé.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="0ce3f-120">False indique qu’un nouveau jeton ou un jeton mis en cache est demandé.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="0ce3f-121">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3f-122">*ppEndpointToken* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ce3f-123">Spécifiez le jeton de point de terminaison à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ce3f-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ce3f-124">Return value</span></span>

<span data-ttu-id="0ce3f-125">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="0ce3f-126">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce3f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="0ce3f-127">Remarks</span></span>

<span data-ttu-id="0ce3f-128">WUA affecte généralement la valeur false au paramètre fRefreshOnline lorsque cette méthode est appelée pour la première fois, puis, si une erreur de connexion se produit, WUA définit ce paramètre sur true lorsque la méthode est à nouveau appelée.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="0ce3f-129">Toutefois, l’implémentation de cette méthode peut demander un nouveau jeton auprès d’un service d’émission de jeton de sécurité (STS) ou fournir un jeton mis en cache à tout moment.</span><span class="sxs-lookup"><span data-stu-id="0ce3f-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce3f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ce3f-130">Requirements</span></span>



| <span data-ttu-id="0ce3f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ce3f-131">Requirement</span></span> | <span data-ttu-id="0ce3f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ce3f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce3f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ce3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce3f-134">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="0ce3f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ce3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce3f-136">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ce3f-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="0ce3f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ce3f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ce3f-138"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ce3f-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="0ce3f-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ce3f-140"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="0ce3f-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ce3f-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ce3f-142"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ce3f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0ce3f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ce3f-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ce3f-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce3f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce3f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce3f-146">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="0ce3f-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




