---
description: Retourne le type de jeton d’authentification par défaut pour le point de terminaison du service.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider :: GetPreferredEndpointTokenType, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201571"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="70a62-103">IUpdateEndpointAuthProvider :: GetPreferredEndpointTokenType, méthode</span><span class="sxs-lookup"><span data-stu-id="70a62-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="70a62-104">Retourne le type de jeton d’authentification par défaut pour le point de terminaison du service.</span><span class="sxs-lookup"><span data-stu-id="70a62-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a62-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70a62-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="70a62-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70a62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a62-107">*ServiceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70a62-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a62-108">Identifie le service à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="70a62-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="70a62-109">*endpointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70a62-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a62-110">Identifie le type de point de terminaison tneeded pour se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="70a62-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="70a62-111">*ulRequestedTypes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70a62-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a62-112">Identifie l’ensemble de jetons qui sont pris en charge par le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="70a62-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="70a62-113">*pulPreferredTokenTypes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="70a62-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70a62-114">Spécifiez l’ensemble de types de jetons d’authentification par défaut.</span><span class="sxs-lookup"><span data-stu-id="70a62-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="70a62-115">(Défini sur 0 pour indiquer qu’aucun jeton d’authentification n’est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="70a62-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a62-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70a62-116">Return value</span></span>

<span data-ttu-id="70a62-117">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="70a62-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="70a62-118">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="70a62-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a62-119">Notes</span><span class="sxs-lookup"><span data-stu-id="70a62-119">Remarks</span></span>

<span data-ttu-id="70a62-120">Lorsque cette méthode est retournée, WUA choisit un type de jeton parmi les types préférés et le transmet au paramètre tokenType de la méthode [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .</span><span class="sxs-lookup"><span data-stu-id="70a62-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a62-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70a62-121">Requirements</span></span>



| <span data-ttu-id="70a62-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70a62-122">Requirement</span></span> | <span data-ttu-id="70a62-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="70a62-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a62-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70a62-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70a62-125">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70a62-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="70a62-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70a62-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70a62-127">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70a62-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="70a62-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="70a62-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a62-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="70a62-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="70a62-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70a62-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="70a62-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70a62-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="70a62-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="70a62-134">DLL</span><span class="sxs-lookup"><span data-stu-id="70a62-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a62-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a62-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70a62-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a62-137">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="70a62-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="70a62-138">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="70a62-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




