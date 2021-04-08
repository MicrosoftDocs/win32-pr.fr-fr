---
description: L’objet RealTimeStylus ne collecte pas l’encre par nature. Pour utiliser l’RealTimeStylus pour collecter l’encre, créez un plug-in de collecteur d’encre.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Plug-ins Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862098"
---
# <a name="ink-collection-plug-ins"></a>Plug-ins Ink-Collection

L’objet [**RealTimeStylus**](realtimestylus-class.md) ne collecte pas l’encre par nature. Pour utiliser l' **RealTimeStylus** pour collecter l’encre, créez un plug-in de collecteur d’encre.

Voici un scénario minimal pour l’utilisation de l’objet [**RealTimeStylus**](realtimestylus-class.md) sur un formulaire qui collecte de l’encre.

1.  Créez un formulaire qui implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Créez un objet [**RealTimeStylus**](realtimestylus-class.md) et attachez-le à un contrôle du formulaire.
3.  Définissez l’intérêt pour les notifications StylusDown, paquets et StylusUp dans la propriété [DataInterest](/previous-versions/ms574886(v=vs.100)) du formulaire.
4.  Dans les méthodes [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)et [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) du formulaire, ajoutez du code pour gérer les notifications de stylet, de paquets et de stylet qui sont envoyées à partir de l’objet [**RealTimeStylus**](realtimestylus-class.md) du formulaire. Ce code doit stocker les données de stylet, et créer et stocker les traits.

Pour obtenir un exemple d’une telle application, consultez exemple d’exemple de [collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> Quand un événement [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) se produit, appelez la méthode [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) des traits collectés dans un gestionnaire d’événements DisplaySettingsChanged pour recalculer les propriétés [Width](/previous-versions/ms582112(v=vs.100)) et [Height](/previous-versions/ms582106(v=vs.100)) . Cela est nécessaire pour tenir compte des modifications possibles en points par pouce (dpi) qui résultent de l’événement DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Collecte et reconnaissance de l’encre

Ni l’analyse de l’encre ni la reconnaissance de l’écriture manuscrite ne sont une fonction de l’objet [**RealTimeStylus**](realtimestylus-class.md) . Lorsque le plug-in Ink-Collector collecte de l’encre ou que vous souhaitez reconnaître l’encre, vous pouvez copier l’encre dans un objet [RecognizerContext](/previous-versions/ms552546(v=vs.100)) ou [diviseur](/previous-versions/ms583616(v=vs.100)) . Pour plus d’informations sur la reconnaissance et l’analyse des encres, consultez à propos de la reconnaissance de l' [écriture manuscrite](about-handwriting-recognition.md) ou [de l’objet de séparateur](the-divider-object.md)

## <a name="static-rendering"></a>Rendu statique

Pour afficher l’encre au fur et à mesure de sa collecte, attachez un objet [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) à l’objet [**RealTimeStylus**](realtimestylus-class.md) . Pour restituer l’encre après qu’elle a été collectée, utilisez un objet de [convertisseur](/previous-versions/ms552630(v=vs.100)) pour dessiner les traits vers l’objet [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) approprié. Pour plus d’informations sur l’objet DynamicRenderer, consultez [plug-ins de rendu dynamique](dynamic-renderer-plug-ins.md). Pour obtenir un exemple de rendu statique et dynamique, consultez [exemple de collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
