---
title: Pourquoi utiliser DirectComposition
description: Cette rubrique décrit les fonctionnalités et les avantages de Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Pourquoi utiliser DirectComposition
- raisons d’utiliser DirectComposition
- Fonctionnalités et avantages de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513734"
---
# <a name="why-use-directcomposition"></a>Pourquoi utiliser DirectComposition ?

> [!NOTE]
> Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique décrit les fonctionnalités et les avantages de Microsoft DirectComposition. Il contient les sections suivantes :

-   [Créer une interface utilisateur attrayante](#create-a-visually-engaging-user-interface)
-   [Activer des animations riches et lisses pour votre application](#enable-rich-smooth-animations-for-your-application)
-   [Combiner des bitmaps de diverses sources](#combine-bitmaps-from-a-variety-of-sources)
-   [Économies de mémoire grâce à l’intégration avec DWM](#memory-savings-though-integration-with-dwm)
-   [Conserver ce que vous avez déjà](#keep-what-you-already-have)
-   [Rubriques connexes](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Créer une interface utilisateur attrayante

DirectComposition vous permet de combiner et d’animer des éléments [*visuels*](directcomposition-glossary.md) pour créer une interface utilisateur visuellement attrayante pour vos applications Windows. Il peut vous aider à donner à votre application une apparence unique, en établissant une identité qui la distingue des autres applications.

DirectComposition peut également aider à faciliter l’utilisation de vos applications. Par exemple, vous pouvez l’utiliser pour créer des signaux visuels et des transitions d’écran animées qui montrent les relations entre les différents éléments à l’écran.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Activer des animations riches et lisses pour votre application

DirectComposition est un moteur de composition bitmap à hautes performances qui utilise des graphiques accélérés par le matériel pour obtenir des fréquences d’images élevées, ce qui permet de lisser et de contourner le panoramique, le défilement et les animations de contenu complexe. Étant donné qu’il opère sur un thread dédié distinct du thread utilisé pour le rendu de l’interface utilisateur de l’application, DirectComposition ne peut jamais « priver » le thread d’interface utilisateur ou interférer avec la capacité de l’application à dessiner ses éléments d’interface utilisateur.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combiner des bitmaps de diverses sources

De nombreuses applications basées sur Windows ont une interface utilisateur qui se compose d’éléments créés par différents frameworks graphiques. Par exemple, une application peut utiliser Windows Forms pour créer une barre d’État, GDI (Windows Graphics Device Interface) pour créer le contenu de la fenêtre principale, Microsoft DirectX pour le contenu graphique, etc. DirectComposition vous permet de combiner le contenu de diverses infrastructures graphiques et de l’afficher dans la même fenêtre de niveau supérieur ou enfant sans avoir à vous soucier de ce qui se passe si le contenu de différents frameworks chevauche.

## <a name="memory-savings-though-integration-with-dwm"></a>Économies de mémoire grâce à l’intégration avec DWM

Les compositions et les animations créées par DirectComposition sont passées à un composant intégré de Windows appelé [Gestionnaire de fenêtrage (DWM)](/windows/desktop/dwm/dwm-overview) pour le rendu à l’écran. Par conséquent, aucun composant de rendu spécial ou infrastructure d’interface utilisateur n’est requis sur l’ordinateur.

## <a name="keep-what-you-already-have"></a>Conserver ce que vous avez déjà

Le code d’interface utilisateur d’une application Windows existante représente un investissement significatif. Pour l’essentiel, DirectComposition vous permet de composer et d’animer le contenu existant de votre interface utilisateur. Cela signifie que vous pouvez utiliser DirectComposition pour effectuer des mises à jour et des améliorations significatives de l’interface utilisateur de votre application sans avoir à apporter de modifications importantes à votre base de code d’interface utilisateur existante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 