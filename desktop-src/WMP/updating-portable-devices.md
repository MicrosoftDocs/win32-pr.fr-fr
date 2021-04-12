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
# <a name="updating-portable-devices"></a>Mise à jour des appareils mobiles

Le lecteur Windows Media permet aux utilisateurs de synchroniser le contenu multimédia numérique avec les périphériques portables. Cela peut inclure du contenu musical acheté ou loué à partir d’un magasin en ligne. Dans certains cas, les fournisseurs de magasins en ligne peuvent souhaiter écrire du code pour travailler sur un appareil mobile connecté dans le cadre de la gestion du contenu fourni par le magasin. Pour que le plug-in de la boutique en ligne puisse travailler avec un appareil connecté, le lecteur Windows Media appelle [IWMPContentPartner :: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) et fournit le nom canonique de l’appareil mobile. Si le code du plug-in détermine qu’un travail doit être effectué avec l’appareil connecté, il doit immédiatement retourner \_ la valeur OK à partir de l’appel à **UpdateDevice** avant de continuer le travail. S’il n’y a pas de travail à effectuer, le plug-in doit retourner un code d’erreur.

Une fois que le plug-in a terminé d’utiliser l’appareil, il doit appeler [IWMPContentPartnerCallback :: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) pour notifier le lecteur Windows Media que l’appareil est disponible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




