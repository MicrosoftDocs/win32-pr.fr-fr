---
title: Utilisation de contrôles Tree-View
description: Cette section contient des détails d’implémentation et un exemple de code pour l’utilisation des contrôles d’arborescence.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8beac9ef5163b52582a2ea89820278cc10f9f68ad865354404efd72a61b04993
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318588"
---
# <a name="using-tree-view-controls"></a>Utilisation de contrôles Tree-View

Cette section contient des détails d’implémentation et un exemple de code pour l’utilisation des contrôles d’arborescence.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comment créer un contrôle de Tree-View](create-a-tree-view-control.md)<br/>       | Pour créer un contrôle Tree-View, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la valeur de l’arborescence [**WC \_**](common-control-window-classes.md) pour la classe Window. La classe de fenêtre d’arborescence est inscrite dans l’espace d’adressage de l’application lors du chargement de la DLL de contrôle commune. Pour vous assurer que la DLL est chargée, utilisez la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) . <br/>                                                                    |
| [Comment initialiser la liste d’images](initialize-the-image-list.md)<br/>         | Chaque élément d’un contrôle Tree-View peut avoir deux images qui lui sont associées. Un élément affiche une image lorsqu’elle est sélectionnée et l’autre quand elle ne l’est pas. Pour inclure des images avec des éléments d’arborescence, utilisez d’abord les fonctions des [listes d’images](image-lists.md) pour créer une liste d’images et y ajouter des images. Associez ensuite la liste d’images au contrôle Tree-View à l’aide du message de [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . <br/>                                                                     |
| [Comment ajouter des éléments de Tree-View](add-tree-view-items.md)<br/>                     | Vous ajoutez un élément à un contrôle Tree-View en envoyant le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) au contrôle. Le message comprend l’adresse d’une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , en spécifiant l’élément parent, l’élément après lequel le nouvel élément est inséré et une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui définit les attributs de l’élément. Les attributs incluent l’étiquette de l’élément, ses images sélectionnées et non sélectionnées, ainsi qu’une valeur 32 bits définie par l’application. <br/> |
| [Comment faire glisser un élément de Tree-View](drag-a-tree-view-item.md)<br/>                 | Cette rubrique montre le code permettant de gérer le glissement et la suppression d’éléments d’arborescence. L’exemple de code se compose de trois fonctions. La première fonction commence l’opération glisser, la deuxième fonction fait glisser l’image et la troisième fonction termine l’opération glisser. <br/>                                                                                                                                                                                                                                  |
| [Utilisation des index d’images d’État](work-with-state-image-indexes.md)<br/> | Il existe souvent une confusion quant à la façon de définir et de récupérer l’index d’images d’État dans un contrôle d’arborescence. Les exemples suivants illustrent la méthode appropriée pour définir et récupérer l’index d’images d’État. Les exemples partent du principe qu’il n’y a que deux index d’images d’État dans le contrôle Tree-View, désactivés et activés. Si votre application en contient plus de deux, ces fonctions devront être modifiées pour gérer ce cas. <br/>                                                               |
| [Utilisation de Tree-View info-bulles](use-tree-view-infotips.md)<br/>               | Lorsque vous appliquez le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) à un contrôle d’arborescence, il génère des notifications [ \_ GETINFOTIP TVN](tvn-getinfotip.md) lorsque le curseur se trouve sur un élément dans l’arborescence. En répondant à cette notification, vous pouvez définir le texte qui apparaît dans l’info-bulle. <br/>                                                                                                                                                                                    |



 

 

