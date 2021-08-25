---
description: Vue d’ensemble des considérations relatives à la conception d’une application qui utilise les interfaces de programmation d’applications (API) StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Considérations relatives à la conception de l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd97a5bad203dd23611acf3d6cb07bead1e1744a10b9ac39afe8a53e65597d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936629"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Considérations relatives à la conception de l’API StylusInput

Voici les éléments à prendre en considération lors de la conception de l’API StylusInput.

-   Vous pouvez mettre à jour la propriété [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) de l’objet [**RealTimeStylus**](realtimestylus-class.md) et la propriété [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) de l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) lorsque le stylet est en cours d’enfoncée. Cela peut être utile lorsque vous souhaitez disposer d’une zone de dessin dynamique pendant que l’application collecte de l’encre.
-   Pour optimiser la réutilisation et la maintenance du code de plug-in, les plug-ins ne doivent pas effectuer d’appels directement à l’application, mais doivent utiliser l’objet [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) ([CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) en code managé) pour communiquer avec l’application.
-   Les collections de plug-ins de l’objet [**RealTimeStylus**](realtimestylus-class.md) sont triées. La position relative de vos plug-ins au sein de ces collections peut être très importante. Par exemple, un plug-in qui modifie les informations de paquet doit probablement être ajouté à la collection de plug-ins synchrone avant un plug-in de rendu dynamique.
-   La possibilité d’ajouter des données de stylet personnalisées au flux de données du stylet doit être utilisée avec modération. Utilisez cette fonctionnalité uniquement si un autre plug-in doit recevoir ces informations dans le cadre du flux de données. Par ailleurs, évitez d’ajouter des données de stylet personnalisées en réponse à d’autres données personnalisées de stylet entrant dans le plug-in, car cela peut créer une boucle infinie.
-   Les collections de plug-ins peuvent être modifiées lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé ; Toutefois, cela peut rendre le comportement de votre application plus difficile à prédire. Quand un plug-in est ajouté alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la fonction Microsoft. StylusInput. IStylusSyncPlugin du plug-in. Méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (méthode [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) dans du code managé). Quand un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** appelle la méthode [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) du plug-in (la méthode [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) dans le code managé). Cela permet au plug-in de conserver son état approprié sans avoir à vérifier la propriété [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) de l’objet **RealTimeStylus** . Quand un plug-in est ajouté alors que l’objet **RealTimeStylus** est activé, les données de plug-in reçues par le plug-in peuvent ne pas contenir suffisamment d’informations pour établir correctement le contexte des données initiales. Par exemple, le plug-in qui vient d’être ajouté peut commencer à recevoir des données de paquets à partir d’un stylet mi-course. De même, lorsqu’un plug-in est supprimé alors que l’objet **RealTimeStylus** est activé, les données de plug-in que le plug-in a reçues sont peut-être insuffisantes pour terminer le traitement des données.
    > [!Note]  
    > Pour la stabilité globale, réinitialisez l’état interne d’un plug-in lorsque sa méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) est appelée.

     

-   L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception si un plug-in modifie la collection de plug-ins à laquelle il est attaché. Cela se produit uniquement lorsque le plug-in le fait pendant qu’il est appelé par l’objet **RealTimeStylus** en tant que membre de cette collection.

 

 
