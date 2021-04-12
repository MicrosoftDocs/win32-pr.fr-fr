---
title: Ajout d’une référence à un projet Visual Basic
description: Ajout d’une référence à un projet Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309733"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Ajout d’une référence à un projet Visual Basic

La procédure suivante décrit comment ajouter une référence à un objet COM à un projet de Visual Basic. Votre application peut ensuite utiliser les classes de cet objet.

Quand vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ». En revanche, l’ajout d’un contrôle en tant que composant expose également les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle.

**Pour créer une référence Visual Basic à un composant**

1.  Dans le menu **Projet**, cliquez sur **Références**.
2.  Activez la case à cocher en regard du composant que vous souhaitez ajouter. Si le composant n’est pas listé, localisez le fichier. dll ou. ocx à l’aide de l’élément **Parcourir**.
3.  Cliquez sur **OK**.

Le composant fait maintenant partie du projet. Votre application peut créer des instances de classe à l’aide du mot clé **New** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout d’un composant à un projet Visual Basic](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Conversion en Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




