---
description: Définit le profil d’analyse spécifié comme profil par défaut.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr :: SetDefault, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533903"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="2c403-103">IScanProfileMgr :: SetDefault, méthode</span><span class="sxs-lookup"><span data-stu-id="2c403-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="2c403-104">Définit le profil d’analyse spécifié comme profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c403-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c403-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c403-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="2c403-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c403-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c403-107">*pScanProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c403-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c403-108">Tapez : \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="2c403-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="2c403-109">Pointeur vers le profil.</span><span class="sxs-lookup"><span data-stu-id="2c403-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c403-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c403-110">Return value</span></span>

<span data-ttu-id="2c403-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2c403-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2c403-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2c403-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c403-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c403-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c403-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2c403-114">Remarks</span></span>

<span data-ttu-id="2c403-115">Utilisez la méthode **IScanProfileMgr :: SetDefault** pour ajouter un `<Default>` élément au profil ou pour supprimer cet élément du profil par défaut précédent de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c403-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="2c403-116">Utilisez la méthode [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) pour modifier le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c403-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c403-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c403-117">Requirements</span></span>



| <span data-ttu-id="2c403-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c403-118">Requirement</span></span> | <span data-ttu-id="2c403-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c403-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c403-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c403-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c403-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c403-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2c403-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c403-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c403-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c403-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c403-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c403-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c403-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c403-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="2c403-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="2c403-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c403-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c403-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c403-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c403-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c403-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="2c403-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="2c403-130">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="2c403-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




