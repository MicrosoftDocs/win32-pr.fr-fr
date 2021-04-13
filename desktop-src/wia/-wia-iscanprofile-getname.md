---
description: Obtient le nom convivial du profil.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'IScanProfile :: GetName, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201670"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="7679d-103">IScanProfile :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="7679d-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="7679d-104">Obtient le nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="7679d-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="7679d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7679d-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="7679d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7679d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7679d-107">*pbstrName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7679d-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7679d-108">Type : \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="7679d-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="7679d-109">Nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="7679d-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7679d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7679d-110">Return value</span></span>

<span data-ttu-id="7679d-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7679d-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7679d-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7679d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7679d-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7679d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7679d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7679d-114">Remarks</span></span>

<span data-ttu-id="7679d-115">Cette méthode est requise car le GUID d’un profil ne peut pas être utilisé pour afficher le profil de numérisation à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7679d-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="7679d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7679d-116">Requirements</span></span>



| <span data-ttu-id="7679d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7679d-117">Requirement</span></span> | <span data-ttu-id="7679d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7679d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7679d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7679d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7679d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7679d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7679d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7679d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7679d-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7679d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7679d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7679d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7679d-124"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7679d-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="7679d-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="7679d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7679d-126"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7679d-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7679d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7679d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7679d-128">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="7679d-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="7679d-129">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="7679d-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




