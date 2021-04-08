---
title: Structure MCI_WAVE_SET_PARMS (Mciapi. h)
description: La structure de l' \_ ensemble des sons MCI Wave \_ contient des \_ informations pour la \_ commande MCI Set pour les périphériques audio Waveform.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Structure de MCI_WAVE_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844226"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="bb3cb-104">Définition de la \_ \_ structure des PARMS MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="bb3cb-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="bb3cb-105">La structure de l' **\_ ensemble des sons MCI Wave \_ \_** contient des informations pour la commande [**MCI \_ Set**](mci-set.md) pour les périphériques audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3cb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb3cb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="bb3cb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bb3cb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb3cb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-111">Format d’heure de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-113">Numéro de canal pour la sortie audio.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-113">Channel number for audio output.</span></span> <span data-ttu-id="bb3cb-114">Généralement utilisé lors de l’activation ou de la désactivation d’un canal.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-115">**wInput**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-116">Canal d’entrée audio.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-117">**wOutput**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-118">Périphérique de sortie à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-118">Output device to use.</span></span> <span data-ttu-id="bb3cb-119">Par exemple, cette valeur peut être 2 si deux cartes son ont été installées sur un système.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-120">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-121">Format des données Waveform-Audio, telles que le \_ format Wave \_ PCM.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="bb3cb-122">Les valeurs possibles sont définies dans mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-124">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-125">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-126">Mono (1) ou stéréo (2).</span><span class="sxs-lookup"><span data-stu-id="bb3cb-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-129">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-130">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-131">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-132">Taux d’échantillonnage en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-134">L’alignement des données est bloqué.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-136">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-137">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-138">Bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-140">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb3cb-141">Notes</span><span class="sxs-lookup"><span data-stu-id="bb3cb-141">Remarks</span></span>

<span data-ttu-id="bb3cb-142">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb3cb-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb3cb-143">Requirements</span></span>



| <span data-ttu-id="bb3cb-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb3cb-144">Requirement</span></span> | <span data-ttu-id="bb3cb-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb3cb-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3cb-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb3cb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3cb-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb3cb-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb3cb-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb3cb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3cb-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb3cb-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb3cb-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb3cb-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb3cb-151"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb3cb-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb3cb-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb3cb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3cb-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bb3cb-154">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bb3cb-155">**jeu de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="bb3cb-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb3cb-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

