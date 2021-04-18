---
description: Indicateurs de profil qui définissent les paramètres de flux pour la topologie de transcodage. Les indicateurs sont définis dans l' \_ \_ énumération de l' \_ énumération des indicateurs de profil de transcodage MF \_ .
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Attribut MF_TRANSCODE_ADJUST_PROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516055"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="ebeb7-104">\_Attribut de \_ profil d’ajustement de TRANScodage MF \_</span><span class="sxs-lookup"><span data-stu-id="ebeb7-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="ebeb7-105">Indicateurs de profil qui définissent les paramètres de flux pour la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="ebeb7-106">Les indicateurs sont définis dans l’énumération de l’énumération des [**\_ \_ \_ \_ indicateurs de profil de transcodage MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .</span><span class="sxs-lookup"><span data-stu-id="ebeb7-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="ebeb7-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ebeb7-107">Data type</span></span>

<span data-ttu-id="ebeb7-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ebeb7-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ebeb7-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ebeb7-109">Get/set</span></span>

<span data-ttu-id="ebeb7-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ebeb7-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ebeb7-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ebeb7-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebeb7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ebeb7-112">Remarks</span></span>

<span data-ttu-id="ebeb7-113">Une application peut définir cet attribut au niveau du conteneur sur le profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="ebeb7-114">Si cet attribut est défini, la fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) modifie les attributs de flux lors de la génération de la topologie, en fonction de l’indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="ebeb7-115">Par exemple, si l’application spécifie l’indicateur d' **\_ \_ ajustement \_ \_ par défaut du profil de transcodage MF** , les paramètres de flux spécifiés par l’application sont utilisés pour créer le profil.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="ebeb7-116">Pour le flux vidéo, la fréquence d’images est mise à jour en fonction de la source du média.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="ebeb7-117">Si l’application ne spécifie pas le mode entrelacé, le profil est mis à jour pour utiliser les trames progressives par défaut.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="ebeb7-118">Si l’application spécifie l’indicateur de **modification de profil d' \_ ajustement de transcodage \_ \_ \_ \_ \_ MF** , les attributs de flux manquants sont copiés de la source du média d’entrée vers les paramètres de flux du profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="ebeb7-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ebeb7-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebeb7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebeb7-120">Requirements</span></span>



| <span data-ttu-id="ebeb7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebeb7-121">Requirement</span></span> | <span data-ttu-id="ebeb7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebeb7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ebeb7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebeb7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ebeb7-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebeb7-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ebeb7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebeb7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ebeb7-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebeb7-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ebeb7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebeb7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebeb7-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebeb7-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebeb7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebeb7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebeb7-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebeb7-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ebeb7-131">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="ebeb7-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="ebeb7-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="ebeb7-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




