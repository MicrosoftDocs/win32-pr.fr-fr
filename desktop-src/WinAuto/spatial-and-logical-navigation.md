---
title: Navigation spatiale et logique
description: Les clients récupèrent des informations sur un objet qui est à proximité ou logiquement proche d’un autre objet dans le même conteneur en appelant IAccessible accNavigate et en spécifiant l’une des constantes de navigation.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d762352c41f2adc764ac40c052632922a25ca995b9f2ec2f5008c668d0332bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052500"
---
# <a name="spatial-and-logical-navigation"></a>Navigation spatiale et logique

Les clients récupèrent des informations sur un objet qui est à proximité ou logiquement proche d’un autre objet dans le même conteneur en appelant [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) et en spécifiant l’une des [constantes de navigation](navigation-constants.md).

Avec les clients de *navigation spatiale* , accédez à un objet en fonction de son emplacement à l’écran. Les clients naviguent vers le haut, vers le haut, à gauche ou à droite de l’objet actuel pour obtenir des informations sur un autre objet dans le même conteneur.

Avec les clients de *navigation logique* , accédez à l’objet qui précède logiquement ou suit un autre objet, comme déterminé par le serveur. Les clients accèdent à tous les enfants d’un objet de deux manières :

-   Démarrez la navigation avec [**NAVDIR \_ firstChild**](navigation-constants.md) , puis appelez à plusieurs reprises la méthode avec [**NAVDIR \_ Next**](navigation-constants.md).
-   Démarrez la navigation avec [**NAVDIR \_ LastChild**](navigation-constants.md) et appelez à plusieurs reprises la méthode avec [**NAVDIR \_ précédent**](navigation-constants.md).

Quelle que soit la direction, la navigation visite chaque enfant visible qui appartient à l’objet parent. Les enfants invisibles peuvent être ignorés avec la navigation logique. En outre, chaque enfant n’est visité qu’une seule fois et la navigation n’est pas en boucle. Autrement dit, la méthode échoue si un client tente de naviguer avant le premier objet ou après le dernier objet.

Les navigations spatiales et logiques sont liées. Par exemple, dans une barre d’outils horizontale, l’appel de la méthode avec [**NAVDIR \_ Right**](navigation-constants.md) doit produire les mêmes résultats que l’appel de la méthode avec [**NAVDIR \_ Next**](navigation-constants.md).

L’objet de départ de la navigation est l’objet lui-même **ou l’un des enfants de l’objet, sauf si** [**NAVDIR \_ firstChild**](navigation-constants.md) ou [**NAVDIR \_ LastChild**](navigation-constants.md) est spécifié ; dans ce cas, la navigation doit commencer à partir de l’objet lui-même.

Si un client navigue d’un objet accessible à un élément d’interface utilisateur frère, ou si le membre **lVal** de *varStart* est **CHILDID \_ Self** et que l’indicateur spécifié dans *navdir* est un indicateur de navigation à l’exception de [**NavDir \_ firstChild**](navigation-constants.md) ou de [**navdir \_ LastChild**](navigation-constants.md), le résultat dans *pvarEnd* est un ID enfant ou une interface [**IDispatch**](idispatch-interface.md) . Si *pvarEnd* contient un ID enfant, les clients doivent d’abord obtenir un pointeur vers l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) du parent pour naviguer à partir de cet élément d’interface utilisateur ou pour obtenir plus d’informations à son sujet. Pour obtenir l’objet parent, les clients appellent la propriété [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) de l’objet frère ou l’objet de départ de la navigation.

Notez que les clients doivent avoir des informations sur tous les objets flottants en appelant la fonction [**EnumChildWindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) . Étant donné qu’un objet flottant n’est pas tronqué à son parent, les clients n’ont pas d’informations sur la relation hiérarchique entre deux objets près l’un de l’autre à l’écran.

Le graphique suivant est un exemple d’objet flottant qui n’est pas coupé à son parent.

![capture d’écran de la fenêtre ouverte flottante au-dessus d’une fenêtre Microsoft Developer Studio plus grande](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Établissement de la commande dans la navigation logique

Dans la navigation logique, les développeurs qui conçoivent les objets établissent les relations entre eux. La navigation logique est plus subjective que la navigation spatiale. En outre, l’ordre dans la navigation logique n’est pas le même que celui utilisé avec les ID enfants.

Pour les objets qui ont des emplacements d’écran, les développeurs de serveurs doivent établir l’ordre de navigation de la façon dont la plupart des utilisateurs considèrent logiquement. Dans les pays/régions anglophones, par exemple, il s’agit d’un ordre de gauche à droite et de haut en bas.

L’ordre de navigation logique doit être l’ordre de navigation au clavier parallèle. Par exemple, une boîte de dialogue contient les boutons **OK** et **Annuler** push et quelques contrôles d’édition. Un client qui appelle [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) pour accéder à l’objet suivant ou précédent dans cette boîte de dialogue se déplace dans le même ordre qu’un utilisateur en appuyant sur Tab ou Maj + Tab pour déplacer le focus entre les éléments.

Pour les objets qui n’ont pas d’emplacements d’écran définis, l’ordre logique est déterminé par les développeurs de serveurs et les développeurs de clients ne doivent pas faire d’hypothèses. Par exemple, il est acceptable pour les objets non visibles, tels que les objets qui sont temporairement masqués, d’être mêlés à des objets visibles.

 

 