---
description: Obtient le nombre d’ID de propriété dans un profil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'IScanProfile :: GetNumPropIDS, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113914"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="08f89-103">IScanProfile :: GetNumPropIDS, méthode</span><span class="sxs-lookup"><span data-stu-id="08f89-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="08f89-104">Obtient le nombre d’ID de propriété dans un profil.</span><span class="sxs-lookup"><span data-stu-id="08f89-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08f89-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="08f89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08f89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f89-107">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="08f89-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08f89-108">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="08f89-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="08f89-109">Nombre d’ID de propriété dans le profil.</span><span class="sxs-lookup"><span data-stu-id="08f89-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f89-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08f89-110">Return value</span></span>

<span data-ttu-id="08f89-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="08f89-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="08f89-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="08f89-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08f89-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08f89-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f89-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08f89-114">Requirements</span></span>



| <span data-ttu-id="08f89-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08f89-115">Requirement</span></span> | <span data-ttu-id="08f89-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="08f89-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f89-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08f89-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08f89-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08f89-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="08f89-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08f89-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08f89-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08f89-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08f89-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="08f89-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="08f89-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f89-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="08f89-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="08f89-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08f89-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08f89-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f89-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08f89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f89-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="08f89-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="08f89-127">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="08f89-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




