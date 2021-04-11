---
description: Supprime le profil de numérisation spécifié.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: IScanProfileMgr ::D méthode eleteProfile (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952070"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="cd57b-103">IScanProfileMgr ::D méthode eleteProfile</span><span class="sxs-lookup"><span data-stu-id="cd57b-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="cd57b-104">Supprime le profil de numérisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd57b-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd57b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd57b-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="cd57b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd57b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd57b-107">*pScanProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd57b-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd57b-108">Tapez : \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="cd57b-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="cd57b-109">Pointeur vers le profil.</span><span class="sxs-lookup"><span data-stu-id="cd57b-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd57b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd57b-110">Return value</span></span>

<span data-ttu-id="cd57b-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cd57b-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cd57b-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd57b-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd57b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd57b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cd57b-114">Remarks</span></span>

<span data-ttu-id="cd57b-115">**IScanProfileMgr ::D eleteprofile** supprime le profil du disque et détruit l’objet de profil en mémoire.</span><span class="sxs-lookup"><span data-stu-id="cd57b-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="cd57b-116">Utilisez la méthode [**IScanProfileMgr :: Refresh**](-wia-iscanprofilemgr-refresh.md) quand plusieurs objets [**IScanProfileMgr**](-wia-iscanprofilemgr.md) peuvent créer ou supprimer des profils en même temps.</span><span class="sxs-lookup"><span data-stu-id="cd57b-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd57b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd57b-117">Requirements</span></span>



| <span data-ttu-id="cd57b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd57b-118">Requirement</span></span> | <span data-ttu-id="cd57b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd57b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd57b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd57b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd57b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cd57b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd57b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd57b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd57b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd57b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd57b-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd57b-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="cd57b-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="cd57b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd57b-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd57b-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd57b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd57b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd57b-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="cd57b-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="cd57b-130">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="cd57b-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




