---
title: Interface IResultType (WdsSharedIDL. h)
description: Expose les informations sur le type de propriété.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- fonctionnalités d’environnement Windows héritées de l’interface IResultType
- fonctionnalités d’environnement Windows héritées de l’interface IResultType, description
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
ms.openlocfilehash: 4c75dd269d19af0cac7318f466a5db11e9e50ea3735594f9aa949130a439fec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014559"
---
# <a name="iresulttype-interface"></a>Interface IResultType

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Lecture seule<br/>  | Cette propriété contient l’identificateur unique pour le type. <br/>                |



 

## <a name="remarks"></a>Remarques

Ces méthodes exposent les types d’informations retournées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

