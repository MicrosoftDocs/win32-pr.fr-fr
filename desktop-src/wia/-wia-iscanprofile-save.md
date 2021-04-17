---
description: Enregistre les modifications apportées à un profil sur le disque.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile :: Save, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527087"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="26ab4-103">IScanProfile :: Save, méthode</span><span class="sxs-lookup"><span data-stu-id="26ab4-103">IScanProfile::Save method</span></span>

<span data-ttu-id="26ab4-104">Enregistre les modifications apportées à un profil sur le disque.</span><span class="sxs-lookup"><span data-stu-id="26ab4-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ab4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ab4-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="26ab4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ab4-106">Parameters</span></span>

<span data-ttu-id="26ab4-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="26ab4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26ab4-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ab4-108">Return value</span></span>

<span data-ttu-id="26ab4-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26ab4-109">Type: **HRESULT**</span></span>

<span data-ttu-id="26ab4-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26ab4-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26ab4-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26ab4-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26ab4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="26ab4-112">Remarks</span></span>

<span data-ttu-id="26ab4-113">Un profil de numérisation enregistré est un fichier XML stocké dans% USERPROFILE% \\ Application Data \\ \\ Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="26ab4-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="26ab4-114">Si plusieurs processus écrivent dans l’objet [**IScanProfile**](-wia-iscanprofile.md) , celui qui appelle **IScanProfile :: Save** Last est le seul processus dont les modifications sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="26ab4-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="26ab4-115">La méthode **IScanProfile :: Save** valide le profil avant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="26ab4-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="26ab4-116">Le profil est toujours considéré comme valide, sauf si la catégorie de l’élément d’acquisition d’images Windows (WIA) 2,0 associé au profil est le \_ chargeur de catégorie WIA ou WIA de la catégorie WIA \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26ab4-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="26ab4-117">Si la catégorie est WIA \_ de catégorie à \_ plat ou WIA \_ \_ , les propriétés suivantes doivent être valides pour l’élément, si les propriétés sont contenues dans le profil :</span><span class="sxs-lookup"><span data-stu-id="26ab4-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="26ab4-118">\_luminosité des adresses IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="26ab4-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="26ab4-119">\_contraste des adresses IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="26ab4-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="26ab4-120">type de données WIA de la \_ Loi WIA \_</span><span class="sxs-lookup"><span data-stu-id="26ab4-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="26ab4-121">\_XRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="26ab4-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="26ab4-122">FORMAT WIA de la \_ Loi WIA \_</span><span class="sxs-lookup"><span data-stu-id="26ab4-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="26ab4-123">En outre, si la catégorie est WIA \_ (alimentation de catégorie WIA \_ ), la \_ propriété de taille de page IPS WIA \_ \_ doit être valide, si elle est présente dans le profil.</span><span class="sxs-lookup"><span data-stu-id="26ab4-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="26ab4-124">Pour plus d’informations sur ces propriétés, consultez [**constantes de propriété d’élément de scanneur WIA**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="26ab4-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26ab4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ab4-125">Requirements</span></span>



| <span data-ttu-id="26ab4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ab4-126">Requirement</span></span> | <span data-ttu-id="26ab4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ab4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ab4-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ab4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26ab4-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ab4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="26ab4-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ab4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26ab4-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ab4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26ab4-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="26ab4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ab4-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ab4-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="26ab4-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="26ab4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26ab4-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26ab4-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ab4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ab4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ab4-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="26ab4-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="26ab4-138">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="26ab4-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




