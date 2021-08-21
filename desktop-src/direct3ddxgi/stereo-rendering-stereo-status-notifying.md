---
description: Les applications ne peuvent pas être rendues en stéréo, sauf si le système d’exploitation indique qu’elle active le comportement d’affichage 3D stéréoscopique. Les applications déterminent si elles doivent être rendues en 3D STEREOSCOPIQUE différemment selon qu’elles sont affichées ou affichées en mode fenêtre.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Rendu en stéréo et notification de l’État stéréo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f17f324a884c5784c98a8f5c21ef9c9dac7b048fc72ae7ed0ea1a75e61e2551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987009"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Rendu en stéréo et notification de l’État stéréo

Les applications ne peuvent pas être rendues en stéréo, sauf si le système d’exploitation indique qu’elle active le comportement d’affichage 3D stéréoscopique. Les applications déterminent si elles doivent être rendues en 3D STEREOSCOPIQUE différemment selon qu’elles sont affichées ou affichées en mode fenêtre.

Une application avec fenêtres appelle la méthode [**IDXGIFactory2 :: IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) pour déterminer s’il faut effectuer le rendu en stéréo. Une application en plein écran appelle la méthode [**IDXGIOutput1 :: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) , puis détermine si l’un des modes d’affichage retournés prend en charge le rendu en stéréo. La méthode **GetDisplayModeList1** n’énumère pas les modes stéréo, sauf si vous spécifiez l’indicateur [**\_ stéréo dxgi enum \_ modes \_**](dxgi-enum-modes.md) dans le paramètre *Flags* . Une application multifenêtre ou plein écran qui prend en charge stéréo commence par effectuer la détermination en mode stéréo en fonction d’un appel à la méthode **IDXGIFactory2 :: IsWindowedStereoEnabled** ou **IDXGIOutput1 :: GetDisplayModeList1** , puis s’inscrit pour la notification des modifications d’État stéréo. Étant donné que l’application ne peut pas compter sur la notification pour indiquer l’état actuel du comportement d’affichage 3D stéréoscopique, lorsqu’elle reçoit un message de notification ou un événement de notification, elle doit appeler **IDXGIFactory2 :: IsWindowedStereoEnabled** ou **IDXGIOutput1 :: GetDisplayModeList1** pour déterminer l’état actuel du comportement d’affichage en 3D stéréoscopique du système d’exploitation.

Si vous souhaitez effectuer un rendu en stéréo, vous devez vous inscrire pour les notifications stéréo afin de savoir quand l’utilisateur désactive ou sur le comportement stéréo. Une application peut s’inscrire pour être avertie des modifications d’État stéréoscopiques 3D par le biais d’un message dans une fenêtre ou par le biais d’une signalisation d’événement. Pour s’inscrire afin de recevoir des messages de notification dans une fenêtre sur les changements d’État stéréo, une application appelle la méthode [**IDXGIFactory2 :: RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) . Pour s’inscrire afin de recevoir la notification des modifications d’État stéréo via la signalisation des événements, une application appelle la méthode [**IDXGIFactory2 :: RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) . Les deux méthodes retournent un pointeur vers une valeur de clé que l’application peut utiliser pour annuler l’inscription de la notification. Pour annuler l’inscription de la notification, l’application passe cette valeur de clé à la méthode [**IDXGIFactory2 :: UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) .

L’État stéréo peut contenir les éléments suivants :

-   Configuration de l’utilisateur.

    Windows les utilisateurs peuvent activer ou désactiver l’affichage stéréo à l’aide de l’option activer le 3d stéréoscopique dans le Paramètres d’affichage des modifications du panneau de configuration.

-   La fonctionnalité et la configuration de l’ordinateur, notamment la carte graphique, le pilote graphique et l’installation de l’analyse.

L' [exemple Direct3D 11,1 simple stéréo 3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) montre comment ajouter un effet stéréoscopique 3D et comment répondre aux modifications du système stéréo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorations de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
