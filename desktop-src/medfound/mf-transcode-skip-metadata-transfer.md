---
description: Spécifie si les métadonnées sont écrites dans le fichier transcodé.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Attribut MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201717"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="8b4b3-103">\_Attribut de \_ \_ transfert de métadonnées Skip de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="8b4b3-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="8b4b3-104">Spécifie si les métadonnées sont écrites dans le fichier transcodé.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="8b4b3-105">Cet attribut de conteneur est stocké dans le profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b4b3-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="8b4b3-106">Data type</span></span>

<span data-ttu-id="8b4b3-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8b4b3-107">**UINT32**</span></span>

<span data-ttu-id="8b4b3-108">Les valeurs possibles pour l' \_ attribut de transfert de métadonnées d’omission de transcodage MF \_ \_ \_ sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="8b4b3-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b4b3-109">Value</span></span>                                                                        | <span data-ttu-id="8b4b3-110">Signification</span><span class="sxs-lookup"><span data-stu-id="8b4b3-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b4b3-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b4b3-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8b4b3-112">Transfère automatiquement les métadonnées au niveau du fichier à partir du fichier source vers le fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="8b4b3-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8b4b3-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8b4b3-114">Les métadonnées du fichier source ne sont pas écrites dans le fichier transcodé.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="8b4b3-115">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="8b4b3-115">Get/set</span></span>

<span data-ttu-id="8b4b3-116">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8b4b3-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8b4b3-117">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8b4b3-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b4b3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8b4b3-118">Remarks</span></span>

<span data-ttu-id="8b4b3-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8b4b3-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4b3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b4b3-120">Requirements</span></span>



| <span data-ttu-id="8b4b3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b4b3-121">Requirement</span></span> | <span data-ttu-id="8b4b3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b4b3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4b3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b4b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4b3-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b4b3-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b4b3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b4b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4b3-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b4b3-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8b4b3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b4b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b4b3-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4b3-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4b3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b4b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4b3-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b4b3-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b4b3-131">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="8b4b3-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="8b4b3-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="8b4b3-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




