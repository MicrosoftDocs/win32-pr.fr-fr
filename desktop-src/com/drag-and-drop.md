---
title: Glisser-déposer
description: Le glisser-déplacer fait référence aux transferts de données dans lesquels une souris ou un autre dispositif de pointage est utilisé pour spécifier la source de données et sa destination.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509389"
---
# <a name="drag-and-drop"></a>Glisser-déposer

Le *glisser-déplacer* fait référence aux transferts de données dans lesquels une souris ou un autre dispositif de pointage est utilisé pour spécifier la source de données et sa destination. Dans une opération de glisser-déplacer classique, un utilisateur sélectionne l’objet à transférer en positionnant le pointeur de la souris sur celui-ci et en maintenant le bouton gauche ou un autre bouton désigné à cet effet. Tout en continuant à maintenir le bouton enfoncé, l’utilisateur lance le transfert en faisant glisser l’objet vers sa destination, qui peut être n’importe quel conteneur OLE. Le glisser-déplacer fournit exactement les mêmes fonctionnalités que le presse-papiers OLE copier et coller, mais ajoute des commentaires visuels et élimine le besoin de menus. En fait, si une application prend en charge le copier-coller du presse-papiers, il est très utile de prendre en charge le glisser-déplacer.

Au cours d’une opération de glisser-déplacer OLE, les trois éléments de code suivants sont utilisés.



| Glisser-déplacer la source du code                               | Implémentation et utilisation                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interface [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implémenté par l’objet contenant les données glissées, appelées « *source de glissement*».<br/>                                                                                         |
| [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) , interface<br/> | Implémenté par l’objet qui est destiné à accepter la suppression, appelée *cible de déplacement*.<br/>                                                                                 |
| [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) , fonction<br/>    | Implémenté par OLE et utilisé pour initier une opération de glisser-déplacer. Une fois l’opération en cours, elle facilite la communication entre la source de glissement et la cible de déplacement.<br/> |



 

Les interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) et [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) peuvent être implémentées dans un conteneur ou dans une application d’objet. Le rôle de la source de glissement ou de la cible de déplacement n’est pas limité à un type d’application OLE.

La fonction OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implémente une boucle qui effectue le suivi du mouvement de la souris et du clavier jusqu’à ce que l’opération glisser soit annulée ou qu’une suppression se produise. **DoDragDrop** est la fonction clé dans le processus de glisser-déplacer, qui facilite la communication entre la source du glissement et la cible du déplacement.

Au cours d’une opération de glisser-déplacer, trois types de commentaires peuvent être affichés à l’utilisateur.



| Type de commentaires            | Description                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commentaires sur la source<br/>  | Fourni par la source de glissement, la rétroaction source indique que les données sont glissées et qu’elles ne changent pas au cours de l’opération de glissement. En règle générale, les données sont mises en surbrillance pour signaler qu’elles ont été sélectionnées.<br/>                                                                                                                                            |
| Commentaires sur le pointeur<br/> | Fourni par la source de glissement, les commentaires du pointeur indiquent ce qui se passe si la souris est relâchée à un moment donné. Les commentaires des pointeurs changent continuellement lorsque l’utilisateur déplace la souris et/ou appuie sur une touche de modification. Par exemple, si le pointeur est déplacé dans une fenêtre qui ne peut pas accepter une suppression, le pointeur se transforme en symbole « non autorisé ».<br/> |
| Commentaires sur la cible<br/>  | Fourni par la cible de déplacement, les commentaires ciblés indiquent où la suppression doit se produire.<br/>                                                                                                                                                                                                                                                                    |



 

Pour plus d’informations, consultez [faire glisser les responsabilités](drag-source-responsibilities.md)de la source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de données](data-transfer.md)
</dt> </dl>

 

 





