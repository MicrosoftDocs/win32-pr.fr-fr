---
description: Définit le GUID de la catégorie d’élément WIA (Windows Image Acquisition) 2,0 à laquelle le profil est associé.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'IScanProfile :: SetItem, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519351"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="ab581-103">IScanProfile :: SetItem, méthode</span><span class="sxs-lookup"><span data-stu-id="ab581-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="ab581-104">Définit le GUID de la catégorie d’élément WIA (Windows Image Acquisition) 2,0 à laquelle le profil est associé.</span><span class="sxs-lookup"><span data-stu-id="ab581-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab581-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab581-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="ab581-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab581-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab581-107">*guidCategory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab581-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab581-108">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="ab581-108">Type: **GUID**</span></span>

<span data-ttu-id="ab581-109">GUID de la catégorie de l’élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="ab581-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="ab581-110">Il doit s’agir de l’une \_ des \_ constantes de catégorie d’élément WIA de la loi WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="ab581-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab581-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab581-111">Return value</span></span>

<span data-ttu-id="ab581-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab581-112">Type: **HRESULT**</span></span>

<span data-ttu-id="ab581-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ab581-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab581-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab581-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab581-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ab581-115">Remarks</span></span>

<span data-ttu-id="ab581-116">Les utilisateurs peuvent modifier la catégorie avec la méthode [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ab581-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="ab581-117">Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="ab581-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="ab581-118">Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="ab581-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab581-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab581-119">Requirements</span></span>



| <span data-ttu-id="ab581-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab581-120">Requirement</span></span> | <span data-ttu-id="ab581-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab581-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab581-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab581-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab581-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab581-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ab581-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab581-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab581-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab581-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab581-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab581-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab581-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab581-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="ab581-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="ab581-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab581-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab581-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab581-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab581-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab581-131">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="ab581-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="ab581-132">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="ab581-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




