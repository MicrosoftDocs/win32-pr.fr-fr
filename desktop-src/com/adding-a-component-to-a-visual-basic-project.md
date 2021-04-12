---
title: Ajout d’un composant à un projet Visual Basic
description: Ajout d’un composant à un projet Visual Basic
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309734"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a>Ajout d’un composant à un projet Visual Basic

La procédure suivante décrit comment ajouter un objet COM en tant que composant à un projet de Visual Basic. Votre application peut ensuite utiliser les classes de cet objet.

L’ajout d’un contrôle en tant que composant expose les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle. En revanche, lorsque vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».

**Pour insérer un contrôle dans un projet Visual Basic**

1.  Dans le menu **Projet**, cliquez sur **Composants**.
2.  Activez la case à cocher en regard du composant que vous souhaitez ajouter. Si le composant n’est pas listé, localisez le fichier. dll ou. ocx à l’aide de l’élément **Parcourir**.
3.  Cliquez sur **OK**.

Le composant fait maintenant partie du projet et s’affiche dans la barre d’outils de l’objet. Votre application peut créer des instances du contrôle en faisant glisser le contrôle à partir de la barre d’outils et en la déposant sur un formulaire ou une boîte de dialogue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout d’une référence à un projet Visual Basic](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[Conversion en Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




