---
title: ajout d’un composant à un Visual Basic Project
description: ajout d’un composant à un Visual Basic Project
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc5adc18570fbe729ed89b5943f8a1d3c3b6c6cb64f1ff54cc72f519f48b7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994069"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a>ajout d’un composant à un Visual Basic Project

la procédure suivante décrit comment ajouter un objet COM en tant que composant à un projet de Visual Basic. Votre application peut ensuite utiliser les classes de cet objet.

l’ajout d’un contrôle en tant que composant expose les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle. En revanche, lorsque vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».

**pour insérer un contrôle dans un projet Visual Basic**

1.  Dans le menu **Projet**, cliquez sur **Composants**.
2.  Activez la case à cocher en regard du composant que vous souhaitez ajouter. Si le composant n’est pas listé, localisez le fichier .dll ou. ocx à l’aide de l’élément **Parcourir**.
3.  Cliquez sur **OK**.

Le composant fait maintenant partie du projet et s’affiche dans la barre d’outils de l’objet. Votre application peut créer des instances du contrôle en faisant glisser le contrôle à partir de la barre d’outils et en la déposant sur un formulaire ou une boîte de dialogue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ajout d’une référence à un Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[Conversion en Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




