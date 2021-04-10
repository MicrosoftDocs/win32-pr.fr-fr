---
title: Direct2D et haute résolution
description: Décrit comment Direct2D prend en charge l’affichage haute résolution.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, haute résolution
- haute résolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941310"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D et haute résolution

L’écriture d’une application prenant en charge DPI est la clé de l’affichage d’une interface utilisateur de manière cohérente sur un large éventail de paramètres d’affichage haute résolution. Une application qui n’a pas de prise en charge DPI mais qui s’exécute sur un paramètre d’affichage haute résolution peut être affectée par un grand nombre d’artefacts visuels, y compris une mise à l’échelle incorrecte des éléments d’interface utilisateur, du texte tronqué et des images floues. En ajoutant la prise en charge dans votre application pour la reconnaissance DPI, vous rendez la présentation de l’interface utilisateur de votre application plus prévisible, ce qui rend plus attrayant et plus facile à lire pour les utilisateurs. Heureusement, Direct2D facilite plus que jamais l’écriture d’applications qui fonctionnent correctement dans la haute résolution. Cette rubrique contient les sections suivantes.

-   [Prise en charge de la haute résolution dans Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 et haute résolution](#windows-8-and-high-dpi)
-   [Qu’est-ce qu’une DIP ?](#what-is-a-dip)
-   [Rubriques connexes](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Prise en charge de la haute résolution dans Direct2D

Direct2D fournit les fonctionnalités suivantes pour l’utilisation de scénarios haute résolution :

-   Il honore automatiquement la résolution du système en cas de création d’une cible de rendu avec fenêtres, tant que le manifeste d’application indique que l’application gère correctement DPI. (Pour plus d’informations sur la façon de déclarer que votre application prend en charge DPI, consultez [Comment garantir que votre application s’affiche correctement sur les affichages haute résolution](how-to--size-a-window-properly-for-high-dpi-displays.md).)
-   Il exprime les coordonnées en DIP (Device Independent Pixel), ce qui permet à l’application de se mettre à l’échelle automatiquement lorsque le paramètre DPI change.
-   Il permet aux bitmaps d’avoir un PPP et de les mettre correctement à l’échelle en tenant compte des PPP. Cette fonctionnalité peut également être utilisée pour gérer les icônes à des résolutions différentes.
-   Il exprime la plupart des ressources dans des DIP, ce qui rend les ressources automatiquement indépendantes de la résolution.
-   Il utilise un espace de coordonnées à virgule flottante et un anticrénelage, de sorte que tout contenu peut être mis à l’échelle en PPP arbitraire.

Le pipeline graphique Direct2D est conçu pour évoluer de 96 PPP à 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 et haute résolution

À compter de Windows 8, il existe des fonctionnalités supplémentaires pour la prise en charge de la haute résolution.

Si le contexte de périphérique PPP est suffisamment élevé, Direct2D modifie le seuil qu’il utilise pour activer l’anticrénelage vertical du texte. Cela aboutit à un rendu de texte plus rapide sur les affichages haute résolution. En outre, vous pouvez basculer le mode d’unité sur les pixels au lieu de DIP à l’aide de la méthode [**ID2D1DeviceContext :: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) . Si vous définissez le mode d’unité sur pixels et le contexte de périphérique sur la résolution d’écran, l’optimisation est toujours activée.

## <a name="what-is-a-dip"></a>Qu’est-ce qu’une DIP ?

Un DIP (Device Independent Pixel) est un pixel logique qui correspond aux pixels de l’appareil physique via une valeur scalaire, la valeur PPP. PPP correspond aux points par pouce, où un point représente un pixel de l’appareil physique. (La nomenclature provient de l’impression, où les points sont le plus petit point d’encre qu’un processus d’impression peut produire). Comme un moniteur standard est utilisé pour 96 points par pouce, une résolution de 96 signifiait qu’un DIP (Device Independent Pixel) soit mappé 1:1 avec un pixel physique. Par exemple, si les PPP étaient 96 \* 2 = 192, un DIP unique englobe deux pixels physiques.

Il existe de nombreuses raisons pour lesquelles les applications ne gèrent pas nécessairement cette mise à l’échelle correctement. l’une des raisons les plus simples est qu’elle nécessite un travail supplémentaire pour découvrir et utiliser cette valeur scalaire lors du rendu. Dans Direct2D, la mise à l’échelle est appliquée par défaut. En raison de ce mappage, les pixels de l’appareil physique peuvent finir par des coordonnées DIP fractionnaires, ce qui est l’une des raisons pour lesquelles Direct2D utilise un espace de coordonnées à virgule flottante.

<dl> Pixel physique = (DIP × DPI)/96  
</dl>

Pour convertir un pixel physique en DIP, utilisez la formule suivante :

<dl> DIP = (pixel physique × 96)/ppp  
</dl>

> [!Note]
>
> À compter de Windows 8, vous pouvez basculer le mode d’unité sur les pixels au lieu de DIP à l’aide de la méthode [**ID2D1DeviceContext :: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment garantir que votre application s’affiche correctement sur les affichages haute résolution](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 