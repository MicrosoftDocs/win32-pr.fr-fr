---
title: Contrôles sans fenêtre
description: Contrôles sans fenêtre
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013035"
---
# <a name="windowless-controls"></a>Contrôles sans fenêtre

la spécification ActiveX controls 96 contient une définition pour les contrôles sans fenêtre. ces contrôles ne fonctionnent pas dans leur propre fenêtre et requièrent qu’un conteneur offre une fenêtre partagée dans laquelle le contrôle peut être dessiné, consultez le kit de développement logiciel (SDK) ActiveX. Les contrôles sans fenêtre sont conçus pour être compatibles avec les conteneurs de contrôle plus anciens en créant leur propre fenêtre dans cette situation, les conteneurs de contrôle sans fenêtre doivent héberger les contrôles de fenêtre de manière traditionnelle sans problème. Il peut toutefois être utile pour un conteneur de distinguer les contrôles qui peuvent fonctionner en mode sans fenêtre, donc une catégorie de composant appropriée est définie.

CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




