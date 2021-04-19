---
description: Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'IScanProfileMgr :: OpenProfile, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524665"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="296c1-103">IScanProfileMgr :: OpenProfile, méthode</span><span class="sxs-lookup"><span data-stu-id="296c1-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="296c1-104">Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="296c1-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="296c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="296c1-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="296c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="296c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="296c1-107">*GUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="296c1-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="296c1-108">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="296c1-108">Type: **GUID**</span></span>

<span data-ttu-id="296c1-109">GUID du profil.</span><span class="sxs-lookup"><span data-stu-id="296c1-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="296c1-110">*ppScanProfile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="296c1-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="296c1-111">Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="296c1-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="296c1-112">Adresse d’un pointeur vers le profil.</span><span class="sxs-lookup"><span data-stu-id="296c1-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="296c1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="296c1-113">Return value</span></span>

<span data-ttu-id="296c1-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="296c1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="296c1-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="296c1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="296c1-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="296c1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="296c1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="296c1-117">Remarks</span></span>

<span data-ttu-id="296c1-118">Si un profil de numérisation est enregistré à l’aide de la méthode [**Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile% \\ Application Data \\ Microsoft \\ document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="296c1-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="296c1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="296c1-119">Requirements</span></span>



| <span data-ttu-id="296c1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="296c1-120">Requirement</span></span> | <span data-ttu-id="296c1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="296c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="296c1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="296c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="296c1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="296c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="296c1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="296c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="296c1-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="296c1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="296c1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="296c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="296c1-127"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="296c1-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="296c1-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="296c1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="296c1-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="296c1-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="296c1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="296c1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="296c1-131">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="296c1-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="296c1-132">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="296c1-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




