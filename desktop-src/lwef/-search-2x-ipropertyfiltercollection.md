---
title: Interface IPropertyFilterCollection (WdsSharedIDL. h)
description: Expose les propriétés de la collection retournée en fonction de la requête envoyée.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, description
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
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349979"
---
# <a name="ipropertyfiltercollection-interface"></a>Interface IPropertyFilterCollection

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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
| [**Count**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Lecture seule<br/>  | Nombre de filtres dans la collection. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lecture/écriture<br/> | Retourne un filtre spécifique dans la collection. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Écriture seule<br/> | Supprime un filtre spécifique de la collection. <br/>     |



 

## <a name="remarks"></a>Remarques

Ces propriétés sont utilisées pour filtrer les collections retournées par la requête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

