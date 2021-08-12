---
description: Le Tablet PC comprend une technologie qui permet d’interagir avec les données du stylet de tablette au fur et à mesure de leur collecte.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Accès et manipulation de l’entrée du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452056"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Accès et manipulation de l’entrée du stylet

Le Tablet PC comprend une technologie qui permet d’interagir avec les données du stylet de tablette au fur et à mesure de leur collecte. La classe [**RealTimeStylus**](realtimestylus-class.md) fait partie des interfaces de programmation d’applications (API) StylusInput qui fournissent l’accès au flux de données de stylet de tablette. Ces API vous permettent de capturer, d’interrompre et de modifier le flux de façon indépendante du rendu et de la collecte de l’encre.

Les API StylusInput sont conçues pour :

-   Fournir un accès en temps réel au flux de données de stylet de tablette.
-   Empêchez le thread d’interface utilisateur de bloquer le rendu d’encre dynamique en mettant en file d’attente les données de paquets sur le thread d’interface utilisateur et en faisant de la collection d’entrée manuscrite un thread unique.
-   Augmentez les performances et réduisez l’utilisation globale des threads par le biais de l’objet [**InkCollector**](inkcollector-class.md) , de l’objet [**InkOverlay**](inkoverlay-class.md) , du contrôle [InkPicture](inkpicture-control-reference.md) ou du contrôle [InkEdit](inkedit-control-reference.md) pour collecter l’encre.

Les API StylusInput ne sont pas conçues pour fonctionner avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) , le contrôle [InkPicture](inkpicture-control-reference.md) ou le contrôle [InkEdit](inkedit-control-reference.md) .

Lorsque vous devez interagir directement avec le flux de données du stylet de tablette ou lorsque votre application peut bloquer l’encrage en temps réel, utilisez l’objet [**RealTimeStylus**](realtimestylus-class.md) . Utilisez l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) , le contrôle [InkPicture](inkpicture-control-reference.md) ou le contrôle [InkEdit](inkedit-control-reference.md) lorsque le comportement par défaut de ces objets fournit le comportement dont vous avez besoin.

## <a name="in-this-section"></a>Dans cette section

Les sections suivantes décrivent les éléments des API StylusInput :

-   [Architecture des API StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Utilisation des API StylusInput](working-with-the-stylusinput-apis.md)
    -   [Utilisation de la classe RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Plug-ins et classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Remarques sur l’implémentation des API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Plug-ins de collection d’encres](ink-collection-plug-ins.md)
    -   [Plug-ins de rendu dynamique](dynamic-renderer-plug-ins.md)
    -   [Plug-ins de reconnaissance](recognizer-plug-ins.md)
-   [Considérations relatives à l’utilisation des API StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Considérations relatives à la conception des API StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Considérations relatives aux threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[Modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md)

-   [Considérations relatives à la gestion des erreurs pour les API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Considérations sur les performances pour les API StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Considérations relatives à la confiance partielle pour les API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Exemple de collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



