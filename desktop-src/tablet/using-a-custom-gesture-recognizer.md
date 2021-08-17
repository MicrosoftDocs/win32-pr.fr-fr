---
description: Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment, ou en plus de GestureRecognizer. Créez votre module de reconnaissance de mouvement personnalisé en tant que IStylusSyncPlugin, faites-le créer CustomStylusData et incluez le plug-in dans le même StylusSyncPluginCollection que le GestureRecognizer. Dans le IStylusSyncPlugin, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Utilisation d’un module de reconnaissance de mouvement personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4c58dd93bdb19f1f930be38e40f0068fa02239f09603035b572559d1f8a916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091300"
---
# <a name="using-a-custom-gesture-recognizer"></a>Utilisation d’un module de reconnaissance de mouvement personnalisé

Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment ou en plus de [**GestureRecognizer**](gesturerecognizer-class.md).

Créez votre module de reconnaissance de mouvement personnalisé en tant que [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), créez-le [CustomStylusData](/previous-versions/ms575208(v=vs.100))et incluez le plug-in dans le même [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que le [**GestureRecognizer**](gesturerecognizer-class.md). Dans le **IStylusSyncPlugin**, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
