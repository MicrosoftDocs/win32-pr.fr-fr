---
description: Obtient le GUID de la catégorie de l’élément WIA (Windows Image Acquisition) 2,0 auquel le profil est associé.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile :: GetItem, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519763"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="64228-103">IScanProfile :: GetItem, méthode</span><span class="sxs-lookup"><span data-stu-id="64228-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="64228-104">Obtient le GUID de la catégorie de l’élément WIA (Windows Image Acquisition) 2,0 auquel le profil est associé.</span><span class="sxs-lookup"><span data-stu-id="64228-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="64228-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64228-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="64228-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64228-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64228-107">*pguidCategory* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64228-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64228-108">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="64228-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="64228-109">Pointeur vers le GUID de la catégorie de l’élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64228-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="64228-110">Il s’agit toujours de l’une \_ des \_ constantes de catégorie d’éléments de la loi WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="64228-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64228-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64228-111">Return value</span></span>

<span data-ttu-id="64228-112">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="64228-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="64228-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64228-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64228-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64228-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="64228-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64228-115">Requirements</span></span>



| <span data-ttu-id="64228-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64228-116">Requirement</span></span> | <span data-ttu-id="64228-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="64228-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64228-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64228-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64228-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64228-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="64228-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64228-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64228-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64228-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64228-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="64228-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="64228-123"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="64228-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="64228-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="64228-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64228-125"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64228-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64228-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64228-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64228-127">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="64228-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="64228-128">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="64228-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




