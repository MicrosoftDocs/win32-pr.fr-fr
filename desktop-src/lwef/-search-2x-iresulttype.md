---
title: Interface IResultType (WdsSharedIDL. h)
description: Expose les informations sur le type de propriété.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultType
- Fonctionnalités d’environnement Windows héritées de l’interface IResultType, Description
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464915"
---
# <a name="iresulttype-interface"></a>Interface IResultType

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Expose les informations sur le type de propriété.

## <a name="members"></a>Membres

L’interface **IResultType** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultType** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IResultType** possède les propriétés suivantes.



| Propriété                                                                 | Type d’accès           | Description                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**NomComplet**](-search-2x-iresulttype-displayname.md)<br/>     | Lecture seule<br/>  | Nom complet localisé du type :<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Lecture/écriture<br/> | Cette propriété contient les informations de propriété spécifiées. <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | Lecture seule<br/>  | Cette propriété contient la chaîne utilisée pour identifier le type dans l’index. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Lecture seule<br/>  | Cette propriété contient le nombre de propriétés exposées par le type. <br/>      |
| [**Identificateur d’utilisateur**](-search-2x-iresulttype-uid.md)<br/>                     | Lecture seule<br/>  | Cette propriété contient l’identificateur unique pour le type. <br/>                |



 

## <a name="remarks"></a>Notes

Ces méthodes exposent les types d’informations retournées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

