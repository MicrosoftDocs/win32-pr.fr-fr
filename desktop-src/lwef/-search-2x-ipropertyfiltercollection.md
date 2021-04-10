---
title: Interface IPropertyFilterCollection (WdsSharedIDL. h)
description: Expose les propriétés de la collection retournée en fonction de la requête envoyée.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, Description
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317318"
---
# <a name="ipropertyfiltercollection-interface"></a>Interface IPropertyFilterCollection

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Expose les propriétés de la collection retournée en fonction de la requête envoyée.

## <a name="members"></a>Membres

L’interface **IPropertyFilterCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilterCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IPropertyFilterCollection** possède les propriétés suivantes.



| Propriété                                                                         | Type d’accès           | Description                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Lecture seule<br/>  | Ajoute un nouveau filtre à la collection. <br/>             |
| [**effacé**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Écriture seule<br/> | Efface la collection. <br/>                           |
| [**Saut**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Lecture seule<br/>  | Nombre de filtres dans la collection. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lecture/écriture<br/> | Retourne un filtre spécifique dans la collection. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Écriture seule<br/> | Supprime un filtre spécifique de la collection. <br/>     |



 

## <a name="remarks"></a>Notes

Ces propriétés sont utilisées pour filtrer les collections retournées par la requête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

