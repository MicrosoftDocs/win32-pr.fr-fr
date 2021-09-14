---
title: ajout d’une référence à un Visual Basic Project
description: ajout d’une référence à un Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232788"
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

 

 




