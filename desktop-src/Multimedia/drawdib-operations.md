---
title: Opérations DrawDib
description: Opérations DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, à propos de
- DrawDib, accès
- DrawDib, ouverture
- DrawDib, opérations
- DrawDib, contexte de périphérique (DC)
- DC (contexte de périphérique)
- DrawDibOpen fonction)
- DrawDibClose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462462"
---
# <a name="drawdib-operations"></a>Opérations DrawDib

Vous pouvez accéder à l’ensemble du groupe de fonctions DrawDib à l’aide de la fonction [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) . Cette fonction charge la bibliothèque de liens dynamiques (DLL), alloue des ressources mémoire, crée un contexte de périphérique (DC) DrawDib et conserve un décompte de références du nombre de contrôleurs de rôle qui sont initialisés. **DrawDibOpen** retourne également un handle du nouveau contrôleur de périphérique que vous utilisez avec les autres fonctions DrawDib.

Vous pouvez libérer un contrôleur de DrawDib quand vous avez fini de l’utiliser à l’aide de la fonction [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) . **DrawDibClose** décrémente également le décompte de références des applications qui accèdent à la dll. L’appel à **DrawDibClose** doit être la dernière fonction DrawDib dans votre application.

Vous pouvez créer autant de contrôleurs de DrawDib que vous le souhaitez. Vous pouvez utiliser plusieurs contrôleurs de DrawDib pour créer plusieurs bitmaps simultanément. Vous pouvez également créer plusieurs contrôleurs de DrawDib, chacun avec des caractéristiques uniques, afin que votre application puisse choisir, puis utiliser le DC avec les paramètres les plus appropriés. Par exemple, vous pouvez créer deux contrôleurs de DrawDib dans une application : un qui affiche une image à sa résolution normale et l’autre qui affiche une partie agrandie de l’image.

Pour s’exécuter efficacement, les fonctions DrawDib requièrent des informations sur la carte d’affichage et son pilote. Le profil d’affichage est obtenu en exécutant une série de tests sur la carte d’affichage la première fois que la DLL contenant les fonctions DrawDib est accédée. Les fonctions DrawDib utilisent ces informations pour toutes les applications. Vous pouvez répéter ces tests si nécessaire à l’aide de la fonction [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .

> [!Note]  
> La récupération et le stockage du profil d’affichage est généralement une occurrence unique. Toutefois, si les informations de profil sont supprimées ou si un autre pilote d’affichage est installé dans le système, DrawDib réexécute les tests.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des fonctions DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




