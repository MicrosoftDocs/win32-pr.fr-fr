---
description: Retourne le GUID du profil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'IScanProfile :: GetGUID, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318581"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="6e608-103">IScanProfile :: GetGUID, méthode</span><span class="sxs-lookup"><span data-stu-id="6e608-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="6e608-104">Retourne le GUID du profil.</span><span class="sxs-lookup"><span data-stu-id="6e608-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e608-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e608-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="6e608-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e608-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e608-107">*retVal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e608-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e608-108">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="6e608-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="6e608-109">Pointeur vers le GUID du profil.</span><span class="sxs-lookup"><span data-stu-id="6e608-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e608-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e608-110">Return value</span></span>

<span data-ttu-id="6e608-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6e608-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6e608-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e608-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e608-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e608-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e608-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6e608-114">Remarks</span></span>

<span data-ttu-id="6e608-115">Le GUID d’un profil est généré automatiquement lors de la création du profil avec [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span><span class="sxs-lookup"><span data-stu-id="6e608-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e608-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e608-116">Requirements</span></span>



| <span data-ttu-id="6e608-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e608-117">Requirement</span></span> | <span data-ttu-id="6e608-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e608-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e608-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e608-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e608-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e608-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6e608-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e608-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e608-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e608-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e608-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e608-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e608-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e608-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="6e608-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="6e608-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e608-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e608-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e608-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e608-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e608-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="6e608-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="6e608-129">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="6e608-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




