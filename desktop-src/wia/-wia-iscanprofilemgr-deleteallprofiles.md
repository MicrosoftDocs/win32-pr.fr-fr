---
description: Supprime tous les profils d’analyse associés à l’appareil spécifié.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: IScanProfileMgr ::D méthode eleteAllProfiles (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034533"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="ff387-103">IScanProfileMgr ::D méthode eleteAllProfiles</span><span class="sxs-lookup"><span data-stu-id="ff387-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="ff387-104">Supprime tous les profils d’analyse associés à l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff387-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff387-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff387-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="ff387-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff387-107">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff387-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff387-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff387-108">Type: **BSTR**</span></span>

<span data-ttu-id="ff387-109">ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ff387-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff387-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff387-110">Return value</span></span>

<span data-ttu-id="ff387-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff387-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ff387-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff387-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff387-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff387-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff387-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff387-114">Requirements</span></span>



| <span data-ttu-id="ff387-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff387-115">Requirement</span></span> | <span data-ttu-id="ff387-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff387-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff387-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff387-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff387-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff387-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ff387-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff387-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff387-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff387-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff387-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff387-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff387-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff387-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="ff387-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="ff387-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff387-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff387-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff387-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff387-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff387-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="ff387-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="ff387-127">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="ff387-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




