---
description: Obtient une valeur qui indique si le profil est le profil de numérisation par défaut d’un appareil IWiaItem2 associé.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'IScanProfile :: IsDefault, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951337"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="c6dcf-103">IScanProfile :: IsDefault, méthode</span><span class="sxs-lookup"><span data-stu-id="c6dcf-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="c6dcf-104">Obtient une valeur qui indique si le profil est le profil de numérisation par défaut d’un appareil [**IWiaItem2**](-wia-iwiaitem2.md) associé.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dcf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6dcf-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="c6dcf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6dcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6dcf-107">*pbDefault* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c6dcf-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dcf-108">Type : \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="c6dcf-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c6dcf-109">Pointeur vers un _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c6dcf-110"><span id="TRUE"></span><span id="true"></span>**:**</span><span class="sxs-lookup"><span data-stu-id="c6dcf-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="c6dcf-111">Le profil est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c6dcf-112"><span id="FALSE"></span><span id="false"></span>**FAUSSES**</span><span class="sxs-lookup"><span data-stu-id="c6dcf-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="c6dcf-113">Le profil n’est pas la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6dcf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6dcf-114">Return value</span></span>

<span data-ttu-id="c6dcf-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6dcf-115">Type: **HRESULT**</span></span>

<span data-ttu-id="c6dcf-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6dcf-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6dcf-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dcf-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c6dcf-118">Remarks</span></span>

<span data-ttu-id="c6dcf-119">*pbDefault* a la **valeur true** si le profil contient un `<Default>` élément.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="c6dcf-120">La **valeur est false** si aucun élément de ce type n’est présent.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="c6dcf-121">L’élément n’a pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dcf-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6dcf-122">Requirements</span></span>



| <span data-ttu-id="c6dcf-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6dcf-123">Requirement</span></span> | <span data-ttu-id="c6dcf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6dcf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dcf-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dcf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dcf-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6dcf-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c6dcf-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6dcf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dcf-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6dcf-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6dcf-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6dcf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6dcf-130"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6dcf-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="c6dcf-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="c6dcf-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6dcf-132"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6dcf-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6dcf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6dcf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dcf-134">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="c6dcf-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="c6dcf-135">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="c6dcf-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




