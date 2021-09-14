---
description: De nombreuses applications permettent aux utilisateurs de transférer des données vers une autre application en les faisant glisser et en les déposant avec la souris, ou à l’aide du presse-papiers.
title: Transfert d’objets Shell avec glisser-déplacer et le presse-papiers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226985"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Transfert d’objets Shell avec glisser-déplacer et le presse-papiers

De nombreuses applications permettent aux utilisateurs de transférer des données vers une autre application en les faisant glisser et en les déposant avec la souris, ou à l’aide du presse-papiers. Parmi les nombreux types de données qu’il est possible de transférer, citons les objets Shell tels que les fichiers ou les dossiers. le transfert de données shell peut avoir lieu entre deux applications, mais les utilisateurs peuvent également transférer des données de l’interpréteur de commandes vers ou à partir du bureau ou de l’explorateur de Windows.

Bien que les fichiers soient l’objet Shell le plus couramment transféré, le transfert de données Shell peut impliquer l’un des nombreux objets trouvés dans l' [espace de noms Shell](namespace-intro.md). Par exemple, votre application peut être amenée à transférer un fichier vers un dossier virtuel, tel que la corbeille, ou à accepter un objet à partir d’une extension d’espace de noms non-Microsoft. Si vous implémentez une extension d’espace de noms, elle doit pouvoir se comporter correctement comme source de déplacement et cible.

Ce document explique comment les applications peuvent implémenter les transferts de données par glisser-déplacer et le presse-papiers avec des objets Shell.

-   [Objet de données de l’interpréteur de commandes](dataobject.md)
-   [Formats de presse-papiers de Shell](clipboard.md)
-   [Gestion des scénarios de transfert de données de Shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Fonctionnement du glisser-déplacer avec les objets Shell

Les applications doivent souvent fournir aux utilisateurs un moyen de transférer des données de l’interpréteur de commandes. Quelques exemples :

-   en faisant glisser un fichier à partir de l’explorateur de Windows ou du bureau, puis en le déposant sur une application.
-   copie d’un fichier dans le presse-papiers dans Windows Explorer et collage dans une application.
-   Glissement d’un fichier d’une application vers la corbeille.

Pour obtenir une présentation détaillée de la façon de gérer ces scénarios et d’autres, consultez Gestion des scénarios de Transfert de données de l' [interpréteur](datascenarios.md)de commandes. Ce document se concentre sur les principes généraux sous-jacents au transfert de données Shell.

Windows offre deux méthodes standard pour le transfert des données de l’interpréteur de commandes :

-   Un utilisateur coupe ou copie des données de l’interpréteur de commandes, par exemple un ou plusieurs fichiers, dans le presse-papiers. L’autre application récupère les données du presse-papiers.
-   Un utilisateur fait glisser une icône qui représente les données de l’application source et dépose l’icône sur une fenêtre appartenant à la cible.

Dans les deux cas, les données transférées sont contenues dans un *objet de données*. Les objets de données sont des objets COM (Component Object Model) qui exposent l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Schématiquement, il existe trois étapes essentielles que tous les transferts de données de Shell doivent suivre :

1.  La source crée un objet de données qui représente les données à transférer.
2.  La cible reçoit un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données.
3.  La cible appelle l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pour en extraire les données.

La différence entre les transferts de données du presse-papiers et du glisser-déplacer réside principalement dans la manière dont le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) est transféré de la source à la cible.

### <a name="clipboard-data-transfers"></a>Transferts de données du presse-papiers

Le presse-papiers est le moyen le plus simple pour transférer des données de Shell. La procédure de base est similaire aux transferts de données du presse-papiers standard. Toutefois, étant donné que vous transférez un pointeur vers un objet de données, et non les données lui-même, vous devez utiliser l’API du presse-papiers OLE au lieu de l’API du presse-papiers standard. La procédure suivante décrit comment utiliser l’API du presse-papiers OLE pour transférer des données de l’interpréteur de commandes avec le presse-papiers :

1.  La source de données crée un objet de données pour contenir les données.
2.  La source de données appelle [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), qui place un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données dans le presse-papiers.
3.  La cible appelle [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) pour récupérer le pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données.
4.  La cible extrait les données en appelant la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) .
5.  Avec certains transferts de données de l’interpréteur de commandes, la cible peut également avoir besoin d’appeler la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données pour fournir des commentaires à l’objet de données sur le résultat du transfert de données. Pour obtenir un exemple de ce type d’opération, consultez [gestion des opérations de déplacement optimisées](datascenarios.md) .

### <a name="drag-and-drop-data-transfers"></a>Transfert de données par glisser-déplacer

Bien qu’un peu plus complexe à implémenter, le transfert de données par glisser-déplacer présente des avantages significatifs par rapport au Presse-papiers :

-   Les transferts par glisser-déplacer peuvent être effectués à l’aide d’un simple déplacement de souris, ce qui rend l’opération plus flexible et intuitive à utiliser que le presse-papiers.
-   Le glisser-déplacer fournit à l’utilisateur une représentation visuelle de l’opération. L’utilisateur peut suivre l’icône lorsqu’il passe de la source à la cible.
-   Le glisser-déplacer notifie la cible lorsque les données sont disponibles.

Les opérations de glisser-déplacer utilisent également des objets de données pour transférer des données. Toutefois, la source de déplacement doit fournir des fonctionnalités au-delà de celles requises pour les transferts du presse-papiers :

-   La source de déplacement doit également créer un objet qui expose une interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Le système utilise **IDropSource** pour communiquer avec la source pendant que l’opération est en cours.
-   L’objet de données glisser-déplacer est chargé de suivre le déplacement du curseur et d’afficher une icône pour représenter l’objet de données.

Les cibles de dépôt doivent également fournir plus de fonctionnalités que nécessaire pour gérer les transferts du presse-papiers :

-   La cible de déplacement doit exposer une interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Lorsque le curseur se trouve sur une fenêtre cible, le système utilise **IDropTarget** pour fournir à la cible des informations telles que la position du curseur et l’avertir lorsque les données sont supprimées.
-   La cible de déplacement doit s’inscrire auprès du système en appelant [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Cette fonction fournit au système le handle d’une fenêtre cible et un pointeur vers l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de l’application cible.

> [!Note]  
> Pour les opérations de glisser-déplacer, votre application doit initialiser COM avec [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), et non [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

La procédure suivante décrit les étapes essentielles qui sont généralement utilisées pour transférer des données de Shell avec le glisser-déplacer :

1.  La cible appelle [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) pour fournir au système un pointeur vers son interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et enregistrer une fenêtre comme cible de déplacement.
2.  Lorsque l’utilisateur démarre une opération de glisser-déplacer, la source crée un objet de données et lance une *boucle de glissement* en appelant [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Lorsque le curseur se trouve sur la fenêtre cible, le système notifie la cible en appelant l’une des méthodes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la cible. Le système appelle [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) lorsque le curseur entre dans la fenêtre cible, et [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) lorsque le curseur passe au-dessus de la fenêtre cible. Les deux méthodes fournissent la cible de déplacement avec la position actuelle du curseur et l’état des touches de modification du clavier, telles que CTRL ou ALT. Lorsque le curseur quitte la fenêtre cible, le système notifie la cible en appelant [**IDropTarget ::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Quand l’une de ces méthodes retourne, le système appelle l’interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) pour passer la valeur de retour à la source.
4.  Quand l’utilisateur relâche le bouton de la souris pour supprimer les données, le système appelle la méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) de la cible. Parmi les paramètres de la méthode se trouve un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données.
5.  La cible appelle la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de l’objet de données pour extraire les données.
6.  Avec certains transferts de données de l’interpréteur de commandes, la cible peut également avoir besoin d’appeler la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données pour fournir des commentaires à la source sur le résultat du transfert de données.
7.  Lorsque la cible est terminée avec l’objet de données, elle retourne à partir de [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). Le système retourne l’appel [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) de la source pour notifier la source que le transfert de données est terminé.
8.  Selon le [scénario de transfert de données](datascenarios.md)particulier, la source devra peut-être effectuer des actions supplémentaires en fonction de la valeur retournée par [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) et des valeurs passées à l’objet de données par la cible. Par exemple, lorsqu’un fichier est déplacé, la source doit vérifier ces valeurs pour déterminer si elle doit supprimer le fichier d’origine.
9.  La source libère l’objet de données.

Bien que les procédures décrites ci-dessus fournissent un bon modèle général pour le transfert de données de Shell, il existe de nombreux types de données différents qui peuvent être contenus dans un objet de données Shell. Il existe également plusieurs scénarios de transfert de données que votre application peut avoir à gérer. Chaque type de données et scénario requiert une approche quelque peu différente de celle des trois étapes clés de la procédure :

-   Comment une source construit un objet de données pour contenir les données de l’interpréteur de commandes.
-   Comment une cible extrait les données de l’interpréteur de commandes de l’objet de données.
-   Comment la source termine l’opération de transfert de données.

L' [objet de données Shell](dataobject.md) fournit une discussion générale sur la manière dont une source construit un objet de données de l’interpréteur de commandes, ainsi que sur la façon dont cet objet de données peut être géré par la cible. [Gestion des scénarios de transfert de données de l’interpréteur](datascenarios.md) de commandes explique en détail comment gérer un certain nombre de scénarios courants de transfert de données Shell.

 

 
