---
title: ajout d’une référence à un Visual Basic Project
description: ajout d’une référence à un Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097069"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>ajout d’une référence à un Visual Basic Project

la procédure suivante décrit comment ajouter une référence à un objet COM à un projet de Visual Basic. Votre application peut ensuite utiliser les classes de cet objet.

Quand vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ». en revanche, l’ajout d’un contrôle en tant que composant expose également les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle.

**pour créer une référence Visual Basic à un composant**

1.  Dans le menu **Projet**, cliquez sur **Références**.
2.  Activez la case à cocher en regard du composant que vous souhaitez ajouter. Si le composant n’est pas listé, localisez le fichier .dll ou. ocx à l’aide de l’élément **Parcourir**.
3.  Cliquez sur **OK**.

Le composant fait maintenant partie du projet. Votre application peut créer des instances de classe à l’aide du mot clé **New** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ajout d’un composant à un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Conversion en Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




