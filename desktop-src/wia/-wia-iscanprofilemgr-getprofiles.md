---
description: Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr :: GetProfiles, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756645"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="fd84f-103">IScanProfileMgr :: GetProfiles, méthode</span><span class="sxs-lookup"><span data-stu-id="fd84f-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="fd84f-104">Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="fd84f-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd84f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd84f-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="fd84f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd84f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd84f-107">*pulNumProfiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd84f-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd84f-108">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="fd84f-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="fd84f-109">En cas de réussite, pointeur vers le nombre maximal de profils à retourner.</span><span class="sxs-lookup"><span data-stu-id="fd84f-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="fd84f-110">En cas de retour, pointeur vers le nombre de profils retournés.</span><span class="sxs-lookup"><span data-stu-id="fd84f-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="fd84f-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd84f-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd84f-112">Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fd84f-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="fd84f-113">Adresse d’un tableau de pointeurs vers des profils.</span><span class="sxs-lookup"><span data-stu-id="fd84f-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd84f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd84f-114">Return value</span></span>

<span data-ttu-id="fd84f-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd84f-115">Type: **HRESULT**</span></span>

<span data-ttu-id="fd84f-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd84f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd84f-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd84f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd84f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fd84f-118">Remarks</span></span>

<span data-ttu-id="fd84f-119">Si le nombre total de profils disponibles pour l’utilisateur est inférieur à la valeur transmise à *pulNumProfiles*, *pulNumProfiles* retourne ce total.</span><span class="sxs-lookup"><span data-stu-id="fd84f-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="fd84f-120">Sinon, elle retourne la même valeur que celle qui lui a été passée.</span><span class="sxs-lookup"><span data-stu-id="fd84f-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd84f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd84f-121">Requirements</span></span>



| <span data-ttu-id="fd84f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd84f-122">Requirement</span></span> | <span data-ttu-id="fd84f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd84f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd84f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd84f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd84f-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd84f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fd84f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd84f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd84f-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd84f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd84f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd84f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd84f-129"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd84f-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="fd84f-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="fd84f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd84f-131"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd84f-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd84f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd84f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd84f-133">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="fd84f-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="fd84f-134">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="fd84f-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




