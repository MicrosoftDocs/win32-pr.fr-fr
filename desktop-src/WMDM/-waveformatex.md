---
title: Structure _WAVEFORMATEX
description: La structure \_WAVEFORMATEX définit le format des données audio .wav.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Structure de _WAVEFORMATEX Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525416"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="56d94-104">\_WAVEFORMATEX, structure</span><span class="sxs-lookup"><span data-stu-id="56d94-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="56d94-105">La structure **\_ WAVEFORMATEX** définit le format des données Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="56d94-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d94-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56d94-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="56d94-107">Membres</span><span class="sxs-lookup"><span data-stu-id="56d94-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="56d94-108">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="56d94-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-109">Doit être défini avec un format ou des formats pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56d94-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="56d94-110">Notez que les versions précédentes du Windows Media Gestionnaire de périphériques recommandé d’utiliser \_ le \_ format WMDM Wave \_ tout pour indiquer la prise en charge de tous les formats.</span><span class="sxs-lookup"><span data-stu-id="56d94-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="56d94-111">Toutefois, cela n’est plus recommandé, car les différents lecteurs multimédias interprètent cela de différentes manières, et quelques appareils peuvent véritablement lire n’importe quel format de fichier.</span><span class="sxs-lookup"><span data-stu-id="56d94-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="56d94-112">Il est maintenant recommandé d’utiliser les valeurs valides de l’énumération WMDM d’énumération \_ \_ \_ \_ \_ n’importe quelle valeur de l’énumération des [**\_ \_ \_ \_ \_ valeurs valides**](wmdm-enum-prop-valid-values-form.md) de l’énumération WMDM, ou de mieux spécifier une plage de formats avec la structure de la [**plage des valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="56d94-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="56d94-113">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="56d94-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-114">Nombre de canaux dans les données audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="56d94-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="56d94-115">Les données mono utilisent un canal et les données stéréo utilisent deux canaux.</span><span class="sxs-lookup"><span data-stu-id="56d94-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="56d94-116">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="56d94-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-117">Taux d’échantillonnage, en échantillons par seconde (Hertz), auquel chaque canal doit être lu ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="56d94-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="56d94-118">Les valeurs courantes pour **nSamplesPerSec** sont 8,0 kilohertz (kHz), 11,025 khz, 22,05 khz et 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="56d94-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="56d94-119">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="56d94-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-120">Taux moyen de transfert de données requis pour la balise format, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="56d94-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="56d94-121">Les logiciels de lecture et d’enregistrement peuvent estimer la taille des mémoires tampons à l’aide du membre **nAvgBytesPerSec** .</span><span class="sxs-lookup"><span data-stu-id="56d94-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="56d94-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="56d94-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-123">Alignement de bloc, en octets.</span><span class="sxs-lookup"><span data-stu-id="56d94-123">Block alignment, in bytes.</span></span> <span data-ttu-id="56d94-124">L’alignement de bloc est l’unité atomique minimale des données pour le type de format **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="56d94-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="56d94-125">Le logiciel de lecture et d’enregistrement doit traiter un multiple de **nBlockAlign** octets de données à la fois.</span><span class="sxs-lookup"><span data-stu-id="56d94-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="56d94-126">Les données écrites et lues à partir d’un appareil doivent toujours commencer au début d’un bloc.</span><span class="sxs-lookup"><span data-stu-id="56d94-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="56d94-127">Par exemple, il n’est pas possible de démarrer correctement les données PCM au milieu d’un échantillon (autrement dit, sur une limite qui n’est pas alignée de bloc).</span><span class="sxs-lookup"><span data-stu-id="56d94-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="56d94-128">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="56d94-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-129">Bits par échantillon pour le type de format **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="56d94-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="56d94-130">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="56d94-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="56d94-131">Ce membre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="56d94-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56d94-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56d94-132">Requirements</span></span>



| <span data-ttu-id="56d94-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56d94-133">Requirement</span></span> | <span data-ttu-id="56d94-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="56d94-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56d94-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="56d94-135">Header</span></span><br/> | <dl> <span data-ttu-id="56d94-136"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56d94-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d94-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56d94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d94-138">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="56d94-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="56d94-139">**IMDSPStorage::CreateStorage**</span><span class="sxs-lookup"><span data-stu-id="56d94-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="56d94-140">**IMDSPStorage :: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="56d94-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="56d94-141">**IWMDMDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="56d94-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="56d94-142">**IWMDMOperation::GetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="56d94-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="56d94-143">**IWMDMOperation::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="56d94-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="56d94-144">**IWMDMStorage :: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="56d94-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="56d94-145">**Structures**</span><span class="sxs-lookup"><span data-stu-id="56d94-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





