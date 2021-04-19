---
description: Les \_ constantes d’indicateur de bit LINEMEDIACONTROL décrivent un ensemble d’opérations génériques sur les flux de média.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526796"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="0c360-103">\_Constantes LINEMEDIACONTROL</span><span class="sxs-lookup"><span data-stu-id="0c360-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="0c360-104">Les constantes d’indicateur de bit **LINEMEDIACONTROL \_** décrivent un ensemble d’opérations génériques sur les flux de média.</span><span class="sxs-lookup"><span data-stu-id="0c360-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="0c360-105">Les interprétations sont déterminées par le flux de média.</span><span class="sxs-lookup"><span data-stu-id="0c360-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="0c360-106">Le périphérique de ligne doit disposer de la fonctionnalité de contrôle de média pour qu’une opération de contrôle de média soit effective.</span><span class="sxs-lookup"><span data-stu-id="0c360-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="0c360-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="0c360-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-108">Aucune modification n’est apportée au flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="0c360-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**\_Pause LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="0c360-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-110">Suspendez temporairement le flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="0c360-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="0c360-111">La vitesse du flux multimédia est retournée à la normale.</span><span class="sxs-lookup"><span data-stu-id="0c360-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**</span><span class="sxs-lookup"><span data-stu-id="0c360-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-113">La vitesse du flux multimédia est réduite par une quantité définie par le flux.</span><span class="sxs-lookup"><span data-stu-id="0c360-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**</span><span class="sxs-lookup"><span data-stu-id="0c360-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**</span><span class="sxs-lookup"><span data-stu-id="0c360-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-116">La vitesse du flux multimédia est augmentée par une quantité définie par le flux.</span><span class="sxs-lookup"><span data-stu-id="0c360-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**\_réinitialisation LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="0c360-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-118">Réinitialisez le flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="0c360-118">Reset the media stream.</span></span> <span data-ttu-id="0c360-119">Équivalent à une fin d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0c360-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="0c360-120">Toutes les mémoires tampons sont libérées.</span><span class="sxs-lookup"><span data-stu-id="0c360-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ Resume**</span><span class="sxs-lookup"><span data-stu-id="0c360-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-122">Reprend un flux de média suspendu.</span><span class="sxs-lookup"><span data-stu-id="0c360-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ Démarrer**</span><span class="sxs-lookup"><span data-stu-id="0c360-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-124">Démarrez le flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="0c360-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**</span><span class="sxs-lookup"><span data-stu-id="0c360-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-126">L’amplitude du flux multimédia est réduite par une quantité définie par le flux.</span><span class="sxs-lookup"><span data-stu-id="0c360-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**</span><span class="sxs-lookup"><span data-stu-id="0c360-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-128">L’amplitude du flux multimédia est retournée à la normale.</span><span class="sxs-lookup"><span data-stu-id="0c360-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c360-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**</span><span class="sxs-lookup"><span data-stu-id="0c360-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c360-130">L’amplitude du flux multimédia est augmentée par une quantité définie par le flux.</span><span class="sxs-lookup"><span data-stu-id="0c360-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c360-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0c360-131">Remarks</span></span>

<span data-ttu-id="0c360-132">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0c360-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="0c360-133">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="0c360-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="0c360-134">Le contrôle de média est fourni pour améliorer les performances des actions sur les flux de média en réponse aux événements liés à la téléphonie.</span><span class="sxs-lookup"><span data-stu-id="0c360-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="0c360-135">L’application doit normalement gérer un flux multimédia via l’API spécifique au média.</span><span class="sxs-lookup"><span data-stu-id="0c360-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="0c360-136">La fonctionnalité de contrôle de média fournie ici n’est pas destinée à remplacer les API de média natives.</span><span class="sxs-lookup"><span data-stu-id="0c360-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="0c360-137">Les actions de contrôle de média peuvent être associées à la détection de chiffres, à la détection de tonalités, à la transition vers un état d’appel et à la détection d’un type de média.</span><span class="sxs-lookup"><span data-stu-id="0c360-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="0c360-138">Consultez les fonctionnalités de l’appareil d’une ligne pour déterminer si le contrôle multimédia est disponible sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="0c360-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c360-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c360-139">Requirements</span></span>



| <span data-ttu-id="0c360-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c360-140">Requirement</span></span> | <span data-ttu-id="0c360-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c360-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0c360-142">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0c360-142">TAPI version</span></span><br/> | <span data-ttu-id="0c360-143">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0c360-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0c360-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c360-144">Header</span></span><br/>       | <dl> <span data-ttu-id="0c360-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c360-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




