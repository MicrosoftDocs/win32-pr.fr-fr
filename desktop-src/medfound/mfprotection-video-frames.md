---
description: Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Attribut MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534189"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="3ec2f-103">\_Attribut de \_ trames vidéo MFPROTECTION</span><span class="sxs-lookup"><span data-stu-id="3ec2f-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="3ec2f-104">Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ec2f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3ec2f-105">Data type</span></span>

<span data-ttu-id="3ec2f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3ec2f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3ec2f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3ec2f-107">Remarks</span></span>

<span data-ttu-id="3ec2f-108">La valeur 0 indique que l’application est autorisée à accéder aux frames.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="3ec2f-109">Cela peut être déterminé à la suite d’un accord privé entre l’application et le système de protection de contenu particulier en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="3ec2f-110">La valeur 1 indique que l’application est autorisée à accéder aux frames si un certificat d’application valide est fourni par l’application (voir [**IMFMediaEngineProtectedContent :: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="3ec2f-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="3ec2f-111">La valeur 0xFFFFFFFF, qui est la valeur par défaut, indique qu’aucune application n’est autorisée à accéder à des frames non compressés.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec2f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ec2f-112">Requirements</span></span>



| <span data-ttu-id="3ec2f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ec2f-113">Requirement</span></span> | <span data-ttu-id="3ec2f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec2f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec2f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec2f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec2f-116">\[Applications UWP Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec2f-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ec2f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec2f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec2f-118">Applications UWP Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec2f-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3ec2f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ec2f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec2f-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec2f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec2f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ec2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec2f-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ec2f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ec2f-123">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="3ec2f-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




