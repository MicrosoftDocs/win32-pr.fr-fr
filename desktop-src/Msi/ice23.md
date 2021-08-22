---
description: ICE23 valide l’ordre de tabulation des contrôles pour chaque boîte de dialogue.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbab2d50c07fce208edc845e64cff0061f513c102a55da2d56b49c4a4c17e867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528999"
---
# <a name="ice23"></a>ICE23

ICE23 valide l’ordre de tabulation des contrôles pour chaque boîte de dialogue.

ICE23 valide les éléments suivants dans la [table de boîtes de dialogue](dialog-table.md) et la [table de contrôle](control-table.md):

-   Que chaque enregistrement dans la table de boîte de dialogue spécifie un contrôle dans la \_ première colonne du contrôle qui existe dans la boîte de dialogue spécifiée par la colonne de la boîte de dialogue.
-   Chaque enregistrement dans la table de contrôle spécifie un contrôle dans la \_ colonne de contrôle suivant qui se trouve dans la même boîte de dialogue que le contrôle figurant dans la colonne de contrôle, ou \_ le contrôle suivant contient la valeur null.
-   Qui suit le contrôle les \_ entrées suivantes du contrôle au contrôle dans la table de contrôle rend une boucle unique et fermée qui revient au contrôle initial. Tous les contrôles ne doivent pas être dans la boucle, mais la boucle doit traverser chaque contrôle qui a une entrée dans la \_ colonne Control Next.

## <a name="result"></a>Résultat

ICE23 publie un message d’erreur si l’ordre de tabulation des contrôles ne constitue pas une boucle fermée unique dans la boîte de dialogue.

## <a name="example"></a>Exemples

ICE23 publie les messages d’erreur suivants pour l’exemple indiqué.

-   Dialog1 n’a pas d’abord de contrôle \_ .
-   Le \_ premier contrôle de la boîte de dialogue Dialog2 fait référence à des ControlX de contrôle inexistants.
-   Dialog3 a un ordre de tabulation de fin mort à l’ControlB de contrôle.
-   Dialog4 a un ordre de tabulation incorrect au niveau du contrôle ControlC
-   Dialog5 a un ordre de tabulation incorrect au niveau du contrôle ControlC.
-   Contrôle \_ en regard du contrôle Dialog6. controlc liens vers un contrôle inconnu.

[Table de boîtes de dialogue](dialog-table.md) (partielle)



| Boîte de dialogue  | \_Premier contrôle |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Table de contrôle](control-table.md) (partielle)



| Boîte de dialogue  | Contrôler  | Contrôle \_ suivant |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | ControlB | ControlA      |
| Dialog2 | ControlA | ControlB      |
| Dialog2 | ControlB | ControlA      |
| Dialog3 | ControlA | ControlB      |
| Dialog3 | ControlB |               |
| Dialog4 | ControlA | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialog5 | ControlA | ControlB      |
| Dialog5 | ControlB | ControlC      |
| Dialog5 | ControlC | ControlA      |
| Dialog5 | En contrôle | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | En contrôle | ControlA      |



 

Pour corriger ces erreurs, notez les points suivants dans les tableaux ci-dessus et apportez les modifications indiquées.

Aucune ligne de la table de boîte de dialogue n’a de contrôle spécifié dans la \_ première colonne du contrôle. Remplacez la \_ première colonne du contrôle de l’enregistrement dialog1 dans la table de boîte de dialogue par un contrôle qui existe dans dialog1.

Les lignes de la table de boîtes de dialogue n’ont pas toutes un contrôle spécifié dans la \_ première colonne du contrôle qui existe dans la boîte de dialogue. Remplacez la \_ première colonne Control de Dialog2 par un contrôle qui existe dans Dialog2.

Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne font pas de boucle fermée dans tous les cas. Modifiez la \_ colonne Control Next de ControlB dans Dialog3 en ControlA.

Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne renvoient pas au contrôle initial dans tous les cas. Modifiez la \_ colonne Control Next de controlc dans Dialog4 pour faire référence à ControlA.

Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne passent pas par chaque contrôle de la boîte de dialogue avec une entrée dans la \_ colonne contrôle suivant. Modifiez la \_ colonne Control Next pour controlc dans Dialog5 en controled.

Control \_ Next ne fait pas référence à un contrôle valide qui se trouve dans la même boîte de dialogue que le contrôle figurant dans la colonne Control. Modifiez la \_ colonne Control Next de controlc dans Dialog6 pour faire référence à controled.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



