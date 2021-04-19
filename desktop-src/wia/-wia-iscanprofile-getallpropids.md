---
description: Obtient tous les ID de propriété disponibles dans un profil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile :: GetAllPropIDs, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524492"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="32236-103">IScanProfile :: GetAllPropIDs, méthode</span><span class="sxs-lookup"><span data-stu-id="32236-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="32236-104">Obtient tous les ID de propriété disponibles dans un profil.</span><span class="sxs-lookup"><span data-stu-id="32236-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="32236-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32236-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="32236-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32236-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32236-107">*nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32236-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32236-108">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="32236-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="32236-109">Nombre d’ID de propriété demandés ou retournés.</span><span class="sxs-lookup"><span data-stu-id="32236-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="32236-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32236-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32236-111">Type : \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="32236-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="32236-112">Pointeur vers un tableau d’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="32236-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32236-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32236-113">Return value</span></span>

<span data-ttu-id="32236-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="32236-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="32236-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32236-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32236-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32236-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32236-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32236-117">Requirements</span></span>



| <span data-ttu-id="32236-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32236-118">Requirement</span></span> | <span data-ttu-id="32236-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="32236-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="32236-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32236-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32236-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32236-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="32236-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32236-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32236-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32236-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32236-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="32236-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32236-125"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="32236-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="32236-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="32236-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32236-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32236-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32236-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32236-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32236-129">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="32236-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="32236-130">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="32236-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




