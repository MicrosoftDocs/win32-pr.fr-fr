---
title: Mise à jour des appareils mobiles
description: Mise à jour des appareils mobiles
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player Online stores, mise à jour des appareils portables
- magasins en ligne, mise à jour des appareils mobiles
- tapez 1 magasins en ligne, mise à jour des appareils portables
- Windows Media Player Online stores, appareils mobiles
- magasins en ligne, appareils mobiles
- tapez 1 magasins en ligne, appareils mobiles
- mise à jour des appareils mobiles
- appareils mobiles, mise à jour
- appareils mobiles, Windows Media Player Online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314227"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="9751d-112">Mise à jour des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="9751d-112">Updating Portable Devices</span></span>

<span data-ttu-id="9751d-113">Le lecteur Windows Media permet aux utilisateurs de synchroniser le contenu multimédia numérique avec les périphériques portables.</span><span class="sxs-lookup"><span data-stu-id="9751d-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="9751d-114">Cela peut inclure du contenu musical acheté ou loué à partir d’un magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="9751d-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="9751d-115">Dans certains cas, les fournisseurs de magasins en ligne peuvent souhaiter écrire du code pour travailler sur un appareil mobile connecté dans le cadre de la gestion du contenu fourni par le magasin.</span><span class="sxs-lookup"><span data-stu-id="9751d-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="9751d-116">Pour que le plug-in de la boutique en ligne puisse travailler avec un appareil connecté, le lecteur Windows Media appelle [IWMPContentPartner :: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) et fournit le nom canonique de l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="9751d-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="9751d-117">Si le code du plug-in détermine qu’un travail doit être effectué avec l’appareil connecté, il doit immédiatement retourner \_ la valeur OK à partir de l’appel à **UpdateDevice** avant de continuer le travail.</span><span class="sxs-lookup"><span data-stu-id="9751d-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="9751d-118">S’il n’y a pas de travail à effectuer, le plug-in doit retourner un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9751d-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="9751d-119">Une fois que le plug-in a terminé d’utiliser l’appareil, il doit appeler [IWMPContentPartnerCallback :: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) pour notifier le lecteur Windows Media que l’appareil est disponible.</span><span class="sxs-lookup"><span data-stu-id="9751d-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9751d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9751d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9751d-121">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="9751d-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




