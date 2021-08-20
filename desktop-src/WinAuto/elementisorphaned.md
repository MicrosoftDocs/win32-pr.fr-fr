---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829368"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Texte

L’élément est un IAccessible orphelin dans l’arborescence

## <a name="type"></a>Type

Erreur

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

 

 




