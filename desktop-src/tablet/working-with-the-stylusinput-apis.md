---
description: La classe RealTimeStylus vous permet d’interagir avec le flux de données à partir du stylet du Tablet PC. Pour interagir avec le flux de données, ajoutez un objet RealTimeStylus à votre application, puis ajoutez des plug-ins à l’objet RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Utilisation des API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143cb885cda16542a65aa096cdf95eb8a187b4f760a916a895887737ec63d7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842839"
---
# <a name="working-with-the-stylusinput-apis"></a>Utilisation des API StylusInput

La classe [**RealTimeStylus**](realtimestylus-class.md) vous permet d’interagir avec le flux de données à partir du stylet du Tablet PC. Pour interagir avec le flux de données, ajoutez un objet **RealTimeStylus** à votre application, puis ajoutez des plug-ins à l’objet **RealTimeStylus** .

Les plug-ins peuvent modifier les données associées aux paquets in-air, au stylet, aux paquets et aux méthodes de notification de stylet. Les plug-ins peuvent annuler les paquets in-air et les méthodes de notification des paquets. Les plug-ins peuvent également ajouter des données d’application au flux sous la forme d’objets [CustomStylusData](/previous-versions/ms575208(v=vs.100)) . La liste suivante fournit des idées pour les catégories courantes de plug-ins que vous pouvez utiliser ou créer.

-   Plug-in de filtre : objet qui supprime ou annule de manière sélective les données dans le flux de données du stylet de tablette.
-   Plug-in de modificateur : objet qui modifie de manière sélective les données dans le flux de données du stylet de tablette.
-   Plug-in de rendu dynamique : objet qui affiche les données du stylet en temps réel, car elles sont gérées par l’objet [**RealTimeStylus**](realtimestylus-class.md) . Plus tard, pour les événements tels qu’une actualisation de formulaire, le plug-in de rendu dynamique ou un plug-in de collection d’encres peut redessiner l’encre.
-   Plug-in de reconnaissance : objet qui analyse le mouvement du stylet du Tablet PC pour les gestes, l’écriture manuscrite ou d’autres glyphes.
-   Plug-in Ink-Collector : un objet issu du flux de données de stylet de tablette crée et stocke l’encre.
-   Plug-in Wrapper : un plug-in qui agit comme une interface entre l’objet [**RealTimeStylus**](realtimestylus-class.md) et un autre plug-in ou objet pour modifier le comportement de l’objet encapsulé.

Les plug-ins de rendu dynamique et de collection d’encres peuvent être créés pour être rendus dans différents contextes, par exemple dans un fichier, un flux ou un périphérique d’affichage. L’encre peut également être stockée dans différents formats, tels qu’un objet [Ink](/previous-versions/aa515768(v=msdn.10)) , un fichier GIF (Graphics Interchange Format) supplémenté, un fichier Ink Serialized Format (ISF) ou d’autres formats.

Deux plug-ins sont fournis avec les API StylusInput : la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) et la classe [**GestureRecognizer**](gesturerecognizer-class.md) . La classe **DynamicRenderer** fournit un rendu de base des données d’encre en temps réel et est rationalisé pour avoir un impact minime sur les performances. La classe **GestureRecognizer** fournit la reconnaissance de mouvement pour la classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="in-this-section"></a>Dans cette section

-   [Utilisation de la classe RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Plug-ins et classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Remarques sur l’implémentation des API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-ins de collection d’encres](ink-collection-plug-ins.md)
-   [Plug-ins de rendu dynamique](dynamic-renderer-plug-ins.md)
-   [Plug-ins de reconnaissance](recognizer-plug-ins.md)

 

 
