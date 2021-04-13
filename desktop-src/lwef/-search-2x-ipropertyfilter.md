---
title: Interface IPropertyFilter (WdsSharedIDL. h)
description: Expose les propriétés utilisées pour filtrer la requête.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter
- Fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter, Description
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508930"
---
# <a name="ipropertyfilter-interface"></a>Interface IPropertyFilter

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Expose les propriétés utilisées pour filtrer la requête.

## <a name="members"></a>Membres

L’interface **IPropertyFilter** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPropertyFilter** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IPropertyFilter** possède les propriétés suivantes.



| Propriété                                                                                      | Type d’accès           | Description                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lecture/écriture<br/> | Nom de la colonne indexée de la propriété sur laquelle filtrer. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lecture/écriture<br/> | Opérateur logique à utiliser lors de l’application d’un filtre. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lecture/écriture<br/> | Filtre la profondeur dans un ensemble imbriqué de parenthèses. <br/> |
| [**IPropertyFilter :: Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lecture/écriture<br/> | Texte du filtre. <br/>                               |
| [**IPropertyFilter :: UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lecture/écriture<br/> | UID de la propriété sur laquelle filtrer. <br/>                 |



 

## <a name="remarks"></a>Notes

Ces propriétés sont utilisées pour filtrer la requête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

