---
description: Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment, ou en plus de GestureRecognizer. Créez votre module de reconnaissance de mouvement personnalisé en tant que IStylusSyncPlugin, faites-le créer CustomStylusData et incluez le plug-in dans le même StylusSyncPluginCollection que le GestureRecognizer. Dans le IStylusSyncPlugin, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Utilisation d’un module de reconnaissance de mouvement personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296010"
---
# <a name="using-a-custom-gesture-recognizer"></a>Utilisation d’un module de reconnaissance de mouvement personnalisé

Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment ou en plus de [**GestureRecognizer**](gesturerecognizer-class.md).

Créez votre module de reconnaissance de mouvement personnalisé en tant que [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), créez-le [CustomStylusData](/previous-versions/ms575208(v=vs.100))et incluez le plug-in dans le même [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que le [**GestureRecognizer**](gesturerecognizer-class.md). Dans le **IStylusSyncPlugin**, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
