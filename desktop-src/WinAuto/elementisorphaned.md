---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512281"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Texte

L’élément est un IAccessible orphelin dans l’arborescence

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet obtenue pour les coordonnées données est une référence à un élément orphelin dans l’arborescence d’éléments.

Ce problème est un problème pour les personnes qui s’appuient sur un lecteur d’écran et un clavier pour la navigation, car les éléments sont traités comme invisibles et ne sont pas annoncés à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.
-   Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Navigation via le test de positionnement et l’emplacement à l’écran](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




