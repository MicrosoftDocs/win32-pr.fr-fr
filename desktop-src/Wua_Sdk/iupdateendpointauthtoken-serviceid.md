---
description: Obtient l’identificateur du service à authentifier avec le jeton de point de terminaison.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'IUpdateEndpointAuthToken :: ServiceID, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517295"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="97ded-103">IUpdateEndpointAuthToken :: ServiceID, méthode</span><span class="sxs-lookup"><span data-stu-id="97ded-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="97ded-104">Obtient l’identificateur du service à authentifier avec le jeton de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="97ded-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ded-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97ded-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="97ded-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ded-107">*pServiceID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97ded-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97ded-108">Identificateur du service.</span><span class="sxs-lookup"><span data-stu-id="97ded-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ded-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97ded-109">Return value</span></span>

<span data-ttu-id="97ded-110">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="97ded-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="97ded-111">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="97ded-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ded-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97ded-112">Requirements</span></span>



| <span data-ttu-id="97ded-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97ded-113">Requirement</span></span> | <span data-ttu-id="97ded-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="97ded-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ded-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97ded-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97ded-116">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97ded-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="97ded-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97ded-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97ded-118">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97ded-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="97ded-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="97ded-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ded-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="97ded-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="97ded-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="97ded-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97ded-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97ded-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="97ded-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97ded-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="97ded-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97ded-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="97ded-125">DLL</span><span class="sxs-lookup"><span data-stu-id="97ded-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97ded-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97ded-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ded-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97ded-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ded-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="97ded-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




