---
description: Énumère à nouveau tous les profils d’analyse dans le système.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'IScanProfileMgr :: Refresh, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951335"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="e7ac7-103">IScanProfileMgr :: Refresh, méthode</span><span class="sxs-lookup"><span data-stu-id="e7ac7-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="e7ac7-104">Énumère à nouveau tous les profils d’analyse dans le système.</span><span class="sxs-lookup"><span data-stu-id="e7ac7-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ac7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7ac7-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="e7ac7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7ac7-106">Parameters</span></span>

<span data-ttu-id="e7ac7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e7ac7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7ac7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7ac7-108">Return value</span></span>

<span data-ttu-id="e7ac7-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7ac7-109">Type: **HRESULT**</span></span>

<span data-ttu-id="e7ac7-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7ac7-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7ac7-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7ac7-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ac7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e7ac7-112">Remarks</span></span>

<span data-ttu-id="e7ac7-113">Utilisez cette méthode lorsque plusieurs objets [**IScanProfileMgr**](-wia-iscanprofilemgr.md) peuvent créer ou supprimer des profils en même temps.</span><span class="sxs-lookup"><span data-stu-id="e7ac7-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ac7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7ac7-114">Requirements</span></span>



| <span data-ttu-id="e7ac7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7ac7-115">Requirement</span></span> | <span data-ttu-id="e7ac7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7ac7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ac7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ac7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ac7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7ac7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e7ac7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ac7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ac7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7ac7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7ac7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7ac7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ac7-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ac7-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="e7ac7-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="e7ac7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7ac7-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7ac7-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ac7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7ac7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ac7-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="e7ac7-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="e7ac7-127">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="e7ac7-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




