---
title: À propos de IWMPPluginEnable
description: À propos de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IWMPPluginEnable
- plug-ins, interface IWMPPluginEnable
- plug-ins de traitement de signal numérique, interface IWMPPluginEnable
- Plug-ins DSP, interface IWMPPluginEnable
- Interface IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939689"
---
# <a name="about-iwmppluginenable"></a>À propos de IWMPPluginEnable

L’interface **IWMPPluginEnable** est requise pour les plug-ins du lecteur Windows Media DSP. **IWMPPluginEnable** contient deux méthodes qui stockent si le lecteur Windows Media a activé le plug-in DSP. Le lecteur Windows Media appelle **IWMPPluginEnable :: SetEnable** lorsqu’il crée une instance du plug-in DSP, en passant la valeur **true** s’il a activé le plug-in ou **false** dans le cas contraire.

Les plug-ins DSP peuvent rester chargés même lorsque l’utilisateur choisit de les désactiver. Lorsqu’il est désactivé, un plug-in doit copier les données de la mémoire tampon d’entrée vers la mémoire tampon de sortie, en effectuant uniquement le traitement de la conversion de format, le cas échéant.

Le lecteur Windows Media appelle également cette méthode avant de libérer une instance du plug-in DSP. Cela est utile pour permettre aux clients du plug-in de vérifier si le plug-in est actuellement activé. Par exemple, un plug-in d’interface utilisateur peut modifier l’apparence de ses contrôles pour alerter l’utilisateur que le plug-in DSP n’est pas connecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces requises**](required-interfaces.md)
</dt> </dl>

 

 




