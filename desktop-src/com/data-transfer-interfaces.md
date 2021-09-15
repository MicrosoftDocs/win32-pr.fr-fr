---
title: Interfaces Transfert de données
description: Interfaces Transfert de données
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530169"
---
# <a name="data-transfer-interfaces"></a>Interfaces Transfert de données

L’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fournit aux consommateurs de données des méthodes permettant d’obtenir et de définir les données d’un objet, de déterminer les formats pris en charge par l’objet, ainsi que d’inscrire et de recevoir des notifications lorsque les données de l’objet sont modifiées. Quand vous obtenez des données, un appelant peut spécifier le format dans lequel il souhaite afficher les données. La source des données, cependant, détermine le support de stockage, qu’elle retourne dans un paramètre de sortie fourni par l’appelant.

à lui seul, [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fournit tous les outils dont vous avez besoin pour implémenter Windows les transferts du presse-papiers ou les transferts de documents composés dans vos applications. Si vous souhaitez également prendre en charge les transferts par glisser-déplacer, vous devez implémenter les interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) et [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) avec **IDataObject**.

l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinée aux api du presse-papiers OLE fournit toutes les fonctionnalités des api Windows presse-papiers. Il n’est généralement pas nécessaire d’utiliser les deux API du presse-papiers. Les fournisseurs de données qui prennent en charge les transferts par glisser-déplacer ou les documents composés OLE doivent implémenter l’interface **IDataObject** . Si votre application ne prend en charge que les transferts du presse-papiers maintenant, mais que vous envisagez d’ajouter des documents de glisser-déplacer ou composés dans des versions ultérieures, vous souhaiterez peut-être implémenter **IDataObject** et les API du presse-papiers OLE maintenant afin de réduire le temps de recodage et de débogage ultérieur. Vous pouvez également implémenter **IDataObject** afin d’utiliser des médias de transfert autres que la mémoire globale.

Le tableau suivant résume les types de transferts de données que vous souhaitez prendre en charge :



| Pour prendre en charge                                                                       | Utilisation                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documents composés<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Glisser-déplacer les transferts<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (ou équivalent)<br/> |
| Transferts du presse-papiers à l’aide de la mémoire globale exclusivement<br/>                   | [API du presse-papiers](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Les transferts du presse-papiers utilisent des supports Exchange autres que la mémoire globale.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Le presse-papiers transfère maintenant, mais glisser-déposer ou des documents composés ultérieurement<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et les interfaces et fonctions mentionnées ci-dessus pour les « transferts par glisser-déplacer »<br/>                                                    |



 

Lorsqu’un utilisateur lance une opération de transfert de données, l’application source crée une instance de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et le rend les données disponibles dans un ou plusieurs formats. Dans un transfert de presse-papiers, l’application appelle la fonction [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) pour passer un pointeur d’objet de données à OLE. (**OleSetClipboard** offre également des formats de données du presse-papiers standard pour les applications OLE version 1 et non-OLE.) Dans un transfert par glisser-déplacer, l’application appelle à la place la fonction [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) .

Du côté réception du transfert, la destination reçoit le pointeur [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) comme argument pour un appel de [**IDropTarget ::D ROP**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) ou en appelant la fonction [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) , selon que le transfert est au moyen d’une opération glisser-déplacer ou du presse-papiers. Après avoir obtenu ce pointeur, la destination appelle [**IDataObject :: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) pour savoir quels formats sont disponibles pour la récupération et sur quels types de supports ils peuvent être obtenus. Avec ces informations, l’application réceptrice demande les données avec un appel à [**IDataObject :: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de données](data-transfer.md)
</dt> </dl>

 

