---
title: À propos de IWMPPluginEnable
description: À propos de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- plug-ins Lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- plug-ins Lecteur Windows Media, interface IWMPPluginEnable
- plug-ins, interface IWMPPluginEnable
- plug-ins de traitement de signal numérique, interface IWMPPluginEnable
- Plug-ins DSP, interface IWMPPluginEnable
- Interface IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa64c811bbc981114f47b6fee15af29a6402594eabec2b857d0098adb8db747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470479"
---
# <a name="about-iwmppluginenable"></a>À propos de IWMPPluginEnable

l’interface **IWMPPluginEnable** est requise pour les plug-ins Lecteur Windows Media DSP. **IWMPPluginEnable** contient deux méthodes qui stockent si Lecteur Windows Media a activé le plug-in DSP. Lecteur Windows Media appelle **IWMPPluginEnable :: SetEnable** lorsqu’il crée une instance du plug-in DSP, en passant la valeur **TRUE** s’il a activé le plug-in ou **false** dans le cas contraire.

Les plug-ins DSP peuvent rester chargés même lorsque l’utilisateur choisit de les désactiver. Lorsqu’il est désactivé, un plug-in doit copier les données de la mémoire tampon d’entrée vers la mémoire tampon de sortie, en effectuant uniquement le traitement de la conversion de format, le cas échéant.

Lecteur Windows Media appelle également cette méthode avant de libérer une instance du plug-in DSP. Cela est utile pour permettre aux clients du plug-in de vérifier si le plug-in est actuellement activé. Par exemple, un plug-in d’interface utilisateur peut modifier l’apparence de ses contrôles pour alerter l’utilisateur que le plug-in DSP n’est pas connecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces requises**](required-interfaces.md)
</dt> </dl>

 

 




