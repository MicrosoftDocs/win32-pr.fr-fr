---
description: Obtient la clé utilisée pour chiffrer les messages sortants protégés par le jeton.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'IUpdateEndpointAuthToken :: SigningKey, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034037"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="a0fd7-103">IUpdateEndpointAuthToken :: SigningKey, méthode</span><span class="sxs-lookup"><span data-stu-id="a0fd7-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="a0fd7-104">Obtient la clé utilisée pour chiffrer les messages sortants protégés par le jeton.</span><span class="sxs-lookup"><span data-stu-id="a0fd7-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fd7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0fd7-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="a0fd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fd7-107">*pbKey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0fd7-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd7-108">Clé utilisée pour chiffrer les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="a0fd7-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd7-109">*pcbKeySize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0fd7-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd7-110">Taille de la clé référencée par le paramètres *pbkey* .</span><span class="sxs-lookup"><span data-stu-id="a0fd7-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0fd7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0fd7-111">Return value</span></span>

<span data-ttu-id="a0fd7-112">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a0fd7-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a0fd7-113">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="a0fd7-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fd7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0fd7-114">Requirements</span></span>



| <span data-ttu-id="a0fd7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0fd7-115">Requirement</span></span> | <span data-ttu-id="a0fd7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0fd7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fd7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0fd7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0fd7-118">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0fd7-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a0fd7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0fd7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0fd7-120">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0fd7-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a0fd7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0fd7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0fd7-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd7-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0fd7-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="a0fd7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0fd7-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd7-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a0fd7-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0fd7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0fd7-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd7-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0fd7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a0fd7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0fd7-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd7-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fd7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0fd7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fd7-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="a0fd7-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




