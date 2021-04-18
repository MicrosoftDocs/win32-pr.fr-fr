---
title: Structure WINBIO_BDB_ANSI_381_HEADER ( \_ types WINBIO. h)
description: Spécifie des informations sur une série d’exemples d’empreintes digitales ou Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BDB_ANSI_381_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512575"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="7cd27-104">\_Structure d' \_ \_ \_ en-tête WINBIO BDB ANSI 381</span><span class="sxs-lookup"><span data-stu-id="7cd27-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="7cd27-105">La structure d' **\_ \_ \_ \_ en-tête WINBIO BDB ANSI 381** spécifie des informations sur une série d’exemples d’empreintes digitales ou Palm.</span><span class="sxs-lookup"><span data-stu-id="7cd27-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd27-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd27-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="7cd27-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7cd27-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cd27-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="7cd27-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-109">Taille, en octets, de cette structure plus la taille de toutes les structures d' [**\_ enregistrement WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) pour les exemples d’empreintes digitales ou Palm capturés par un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="7cd27-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="7cd27-110">Seuls les six octets de poids faible sont valides.</span><span class="sxs-lookup"><span data-stu-id="7cd27-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-111">**FormatIdentifier**</span><span class="sxs-lookup"><span data-stu-id="7cd27-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-112">Spécifie le format.</span><span class="sxs-lookup"><span data-stu-id="7cd27-112">Specifies the format.</span></span> <span data-ttu-id="7cd27-113">Actuellement, il doit s’agir de 0x46495200.</span><span class="sxs-lookup"><span data-stu-id="7cd27-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-114">**NuméroVersion**</span><span class="sxs-lookup"><span data-stu-id="7cd27-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-115">Spécifie le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="7cd27-115">Specifies the version number.</span></span> <span data-ttu-id="7cd27-116">À l’heure actuelle, ce doit être 0x30313000 qui correspond en interne à 0.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="7cd27-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="7cd27-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-118">Structure [**de \_ \_ format inscrite WINBIO**](winbio-registered-format.md) qui contient le format de données inscrit sous la forme d’une paire propriétaire/type.</span><span class="sxs-lookup"><span data-stu-id="7cd27-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-119">**CaptureDeviceId**</span><span class="sxs-lookup"><span data-stu-id="7cd27-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-120">Contient l’ID d’unité de l’appareil utilisé pour capturer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7cd27-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-121">**ImageAcquisitionLevel**</span><span class="sxs-lookup"><span data-stu-id="7cd27-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-122">Spécifie le niveau de résolution à partir duquel l’échantillon est capturé.</span><span class="sxs-lookup"><span data-stu-id="7cd27-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-123">**HorizontalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="7cd27-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-124">Spécifie la résolution horizontale de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7cd27-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-125">**VerticalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="7cd27-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-126">Spécifie la résolution verticale de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7cd27-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-127">**HorizontalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="7cd27-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-128">Spécifie la résolution horizontale de l’empreinte digitale ou de l’image Palm capturée.</span><span class="sxs-lookup"><span data-stu-id="7cd27-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-129">**VerticalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="7cd27-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-130">Spécifie la résolution verticale de l’empreinte digitale ou de l’image Palm capturée.</span><span class="sxs-lookup"><span data-stu-id="7cd27-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-131">**ElementCount**</span><span class="sxs-lookup"><span data-stu-id="7cd27-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-132">Nombre d’enregistrements Finger ou Palm dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="7cd27-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-133">**ScaleUnits**</span><span class="sxs-lookup"><span data-stu-id="7cd27-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-134">Contient l’unité de mesure, 1 pour les pouces et 2 pour les centimètres.</span><span class="sxs-lookup"><span data-stu-id="7cd27-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-135">**PixelDepth**</span><span class="sxs-lookup"><span data-stu-id="7cd27-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-136">Spécifie le nombre de bits dans un pixel.</span><span class="sxs-lookup"><span data-stu-id="7cd27-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="7cd27-137">Il peut s’agir de 1 à 16 bits par pixel pour la couleur.</span><span class="sxs-lookup"><span data-stu-id="7cd27-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-138">**ImageCompressionAlg**</span><span class="sxs-lookup"><span data-stu-id="7cd27-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="7cd27-139">Spécifie l’algorithme utilisé pour compresser l’image de doigt ou Palm.</span><span class="sxs-lookup"><span data-stu-id="7cd27-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="7cd27-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7cd27-140">**Reserved**</span></span>
<span data-ttu-id="7cd27-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7cd27-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7cd27-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd27-142">Requirements</span></span>



| <span data-ttu-id="7cd27-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd27-143">Requirement</span></span> | <span data-ttu-id="7cd27-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd27-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd27-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd27-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd27-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd27-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7cd27-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd27-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd27-148">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd27-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7cd27-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cd27-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd27-150"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cd27-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd27-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd27-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd27-152">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="7cd27-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





