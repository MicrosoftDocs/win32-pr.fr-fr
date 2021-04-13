---
title: Implémentation d’autres fonctions
description: Implémentation d’autres fonctions
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- visualisations, interface IWMPEffects
- visualisations personnalisées, interface IWMPEffects
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Fonction Render, fonctions supplémentaires
- Interface IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed6efa5cc9a0697653e558f27165b66d5f230fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381527"
---
# <a name="implementing-other-functions"></a>Implémentation d’autres fonctions

Vous souhaiterez sans aucun doute écrire votre propre implémentation de la fonction **Render** . Plusieurs autres fonctions qui sont également des fonctions membres de l’interface **IWMPEffects** sont fournies. Certains vous fourniront des informations supplémentaires que vous pouvez choisir d’utiliser et d’autres fourniront automatiquement le lecteur Windows Media avec les informations générées par l’Assistant, telles que le nom de votre visualisation.

L’interface **IWMPEffects** prend en charge les fonctions suivantes, en plus du **rendu**:



| Fonction                                                   | Description                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implémentation par défaut non fournie par l’Assistant.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Obtient les fonctionnalités de votre visualisation et les transmet au lecteur Windows Media.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | L’Assistant a créé deux présélections lorsqu’il a généré le code pour votre visualisation. Cette fonction est appelée lorsque le développeur de l’apparence souhaite obtenir l’index de la présélection actuelle. Vous ne souhaitez pas modifier l’implémentation de cette fonction, car elle utilise simplement les informations définies par d’autres fonctions. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | L’Assistant a créé deux présélections lorsqu’il a généré le code pour votre visualisation. Vous pouvez modifier le nombre en modifiant l’implémentation de **GetPresetCount**. Pour plus d’informations sur la modification des présélections, consultez [présélections](presets.md) .                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | L’Assistant a créé deux présélections lorsqu’il a généré le code pour votre visualisation. Vous pouvez modifier les titres utilisés en modifiant l’implémentation de **GetPresetTitle**. Pour plus d’informations sur la modification des présélections, consultez [présélections](presets.md) .                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Obtient le titre de votre visualisation et le transmet au lecteur Windows Media. L’Assistant a utilisé le nom de votre projet pour générer le nom qui est renvoyé.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implémentation par défaut non fournie par l’Assistant.                                                                                                                                                                                                                                                           |
| [MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Récupère le nombre de canaux audio et le taux d’échantillonnage du son en cours de lecture.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implémentation par défaut non fournie par l’Assistant.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | L’Assistant a créé deux présélections lorsqu’il a généré le code pour votre visualisation. Cette fonction est appelée lorsque le lecteur Windows Media souhaite passer à une présélection nommée.                                                                                                                                   |



 

L’interface **IWMPEffects2** prend en charge les fonctions supplémentaires suivantes :



| Fonction                                            | Description                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Créer](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Lors du rendu dans une fenêtre, le lecteur Windows Media appelle cette fonction pour vous permettre de créer une nouvelle fenêtre de rendu.                          |
| [Suppression](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Lors du rendu dans une fenêtre, le lecteur Windows Media appelle cette fonction pour vous permettre de détruire la fenêtre que vous avez créée lors de l’appel de **Create** . |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Cette fonction permet à votre visualisation de répondre lorsqu’un nouvel élément multimédia a été chargé par le joueur.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Cette fonction reçoit les messages Windows du lecteur lors du rendu en mode sans fenêtre.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Cette fonction est appelée par le joueur au lieu de **IWMPEffects :: Render** lorsque le lecteur est rendu en mode fenêtre.                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Cette fonction reçoit un pointeur vers l’interface **IWMPCore** .                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de votre code**](implementing-your-code.md)
</dt> </dl>

 

 




