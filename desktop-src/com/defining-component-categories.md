---
title: Définition des catégories de composants
description: Définition des catégories de composants
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840c785f4b263f0288793f62542cc6d93637b719ff37c9cf29454f43dfaa1914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071009"
---
# <a name="defining-component-categories"></a>Définition des catégories de composants

L’auteur d’une définition de catégorie de composant crée un GUID unique (le CATID) qui est publié avec la définition. Les autres parties connaissent la définition de ce type et peuvent utiliser ses classes prises en charge en conséquence. À l’instar de la signature de méthode d’une interface, la sémantique d’une catégorie ne doit pas être modifiée après son installation. Il est préférable de conserver la compatibilité descendante de la catégorie en introduisant un nouvel identificateur de catégorie avec la sémantique révisée.

Étant donné que les identificateurs d’interface (IID) et les identificateurs de catégories de composants (CATID) existent dans des espaces de noms différents, il semble qu’il soit possible d’utiliser le même GUID pour un IID et un CATID. Toutefois, étant donné que les IID sont souvent utilisés pour le CLSID du serveur proxy/stub de l’interface, il y a un risque de conflit. Par conséquent, n’utilisez pas le même GUID pour un IID et un CATID.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Association d’icônes à une catégorie](associating-icons-with-a-category.md)
</dt> <dt>

[Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
</dt> <dt>

[Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes et associations par défaut](default-classes-and-associations.md)
</dt> <dt>

[Gestionnaire de catégories de composants](the-component-categories-manager.md)
</dt> </dl>

 

 




