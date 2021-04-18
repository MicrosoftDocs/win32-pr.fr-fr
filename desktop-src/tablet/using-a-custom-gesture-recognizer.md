---
description: Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment, ou en plus de GestureRecognizer. Créez votre module de reconnaissance de mouvement personnalisé en tant que IStylusSyncPlugin, faites-le créer CustomStylusData et incluez le plug-in dans le même StylusSyncPluginCollection que le GestureRecognizer. Dans le IStylusSyncPlugin, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Utilisation d’un module de reconnaissance de mouvement personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519286"
---
# <a name="using-a-custom-gesture-recognizer"></a><span data-ttu-id="0be23-104">Utilisation d’un module de reconnaissance de mouvement personnalisé</span><span class="sxs-lookup"><span data-stu-id="0be23-104">Using a Custom Gesture Recognizer</span></span>

<span data-ttu-id="0be23-105">Vous pouvez utiliser un module de reconnaissance de mouvement personnalisé indépendamment ou en plus de [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="0be23-105">You can use a custom gesture recognizer independently, or in addition to the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span>

<span data-ttu-id="0be23-106">Créez votre module de reconnaissance de mouvement personnalisé en tant que [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), créez-le [CustomStylusData](/previous-versions/ms575208(v=vs.100))et incluez le plug-in dans le même [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que le [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="0be23-106">Create your custom gesture recognizer as an [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), have it create [CustomStylusData](/previous-versions/ms575208(v=vs.100)), and include the plug-in in the same [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) as the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span> <span data-ttu-id="0be23-107">Dans le **IStylusSyncPlugin**, combinez les notifications de mouvement des deux regroupements dans les notifications à consommer par une application.</span><span class="sxs-lookup"><span data-stu-id="0be23-107">In the **IStylusSyncPlugin**, combine gesture notifications from both recognizers into notifications to be consumed by an application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0be23-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0be23-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be23-109">Accès et manipulation de l’entrée du stylet</span><span class="sxs-lookup"><span data-stu-id="0be23-109">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
