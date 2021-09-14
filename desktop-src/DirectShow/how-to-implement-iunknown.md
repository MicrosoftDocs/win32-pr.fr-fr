---
description: Comment implémenter IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Comment implémenter IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119857"
---
# <a name="how-to-implement-iunknown"></a>Comment implémenter IUnknown

Microsoft DirectShow est basé sur le modèle COM (component Object Model). Si vous écrivez votre propre filtre, vous devez l’implémenter en tant qu’objet COM. les classes de base DirectShow fournissent une infrastructure à partir de laquelle effectuer cette opération. L’utilisation des classes de base n’est pas obligatoire, mais elle peut simplifier le processus de développement. cet article décrit quelques-uns des détails internes des objets COM et leur implémentation dans les classes de base DirectShow.

Cet article suppose que vous savez comment programmer des applications clientes COM, en d’autres termes, que vous comprenez les méthodes dans **IUnknown**, mais ne suppose pas d’expérience préalable du développement d’objets com. DirectShow gère un grand nombre des détails du développement d’un objet COM. Si vous avez des difficultés à développer des objets COM, vous devez lire la section [à l’aide de CUnknown](using-cunknown.md), qui décrit la classe de base [**CUnknown**](cunknown.md) .

COM est une spécification, et non une implémentation. Il définit les règles qu’un composant doit suivre ; le fait de placer ces règles en vigueur est laissé au développeur. dans DirectShow, tous les objets dérivent d’un ensemble de classes de base C++. Les constructeurs et les méthodes de la classe de base effectuent la plupart des tâches de « comptabilité » COM, telles que la conservation d’un décompte de références cohérent. En dérivant votre filtre à partir d’une classe de base, vous héritez des fonctionnalités de la classe. Pour utiliser efficacement les classes de base, vous avez besoin d’une compréhension générale de la façon dont elles implémentent la spécification COM.

Cet article contient les rubriques suivantes.

-   [Fonctionnement de IUnknown](how-iunknown-works.md)
-   [Utilisation de CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow et COM](directshow-and-com.md)
</dt> </dl>

 

 



