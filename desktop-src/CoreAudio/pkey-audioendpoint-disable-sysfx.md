---
description: La \_ propriété AudioEndpoint de la \_ fonction de désactivation \_ de SysFx spécifie si les effets système sont activés dans le flux en mode partagé qui circule vers ou à partir de l’appareil de point de terminaison audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111194"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="1a727-103">AudioEndpoint de la \_ \_ SysFx de désactivation \_</span><span class="sxs-lookup"><span data-stu-id="1a727-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="1a727-104">La propriété AudioEndpoint de la fonction de **\_ \_ désactivation de \_ SysFx** spécifie si les effets système sont activés dans le flux en mode partagé qui circule vers ou à partir de l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="1a727-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="1a727-105">Les effets système sont implémentés en tant qu’objets de traitement audio (APOs) qui peuvent être insérés dans un flux audio.</span><span class="sxs-lookup"><span data-stu-id="1a727-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="1a727-106">APOs sont des modules logiciels qui exécutent des fonctions de traitement audio, telles que le contrôle de volume et la conversion de format.</span><span class="sxs-lookup"><span data-stu-id="1a727-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="1a727-107">La désactivation des effets système pour un appareil de point de terminaison permet au flux associé de traverser l’APOs non modifié.</span><span class="sxs-lookup"><span data-stu-id="1a727-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="1a727-108">Pour plus d’informations sur les effets système dans Windows Vista, consultez les livres blancs intitulés « effets audio personnalisés dans Windows Vista » et « réutilisation de Windows Vista Audio Effects » sur le site Web [des technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="1a727-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="1a727-109">Cette propriété s’applique uniquement aux effets locaux et aux effets globaux APOs qui ont été installés par le fichier. inf qui a installé la carte audio à laquelle l’appareil de point de terminaison est connecté.</span><span class="sxs-lookup"><span data-stu-id="1a727-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="1a727-110">En outre, cette propriété affecte uniquement l’appareil de point de terminaison cible. elle n’a aucun effet sur les effets système pour les autres appareils de point de terminaison, même s’ils se connectent au même adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1a727-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="1a727-111">Le membre **VT** de la structure **PROPVARIANT** est défini sur **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="1a727-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="1a727-112">Le membre **ulVal** de la structure **PROPVARIANT** est défini sur **Endpoint \_ SYSFX \_ activé** si les effets système sont activés ou sur le **point de terminaison \_ SYSFX \_ désactivé** s’ils sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="1a727-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a727-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a727-113">Requirements</span></span>



| <span data-ttu-id="1a727-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a727-114">Requirement</span></span> | <span data-ttu-id="1a727-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a727-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a727-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a727-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a727-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a727-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1a727-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a727-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a727-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a727-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1a727-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a727-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a727-121"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a727-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a727-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a727-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a727-123">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="1a727-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="1a727-124">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="1a727-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




