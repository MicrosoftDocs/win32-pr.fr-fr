---
title: Interface IResultProperty (WdsSharedIDL. h)
description: Expose les propriétés de résultat.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- fonctionnalités d’environnement Windows héritées de l’interface IResultProperty
- fonctionnalités d’environnement Windows héritées de l’interface IResultProperty, description
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754582"
---
# <a name="iresultproperty-interface"></a>Interface IResultProperty

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Expose les propriétés de résultat.

## <a name="members"></a>Membres

L’interface **IResultProperty** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultProperty** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IResultProperty** possède ces méthodes.



| Méthode                                                    | Description                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Non implémenté.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Non implémenté.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IResultProperty** possède les propriétés suivantes.



| Propriété                                                                   | Type d’accès          | Description                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Décimal**](-search-2x-iresultproperty-datatype.md)<br/>         | Lecture seule<br/> | Type de données des propriétés. <br/>                   |
| [**NomComplet**](-search-2x-iresultproperty-displayname.md)<br/>   | Lecture seule<br/> | Nom complet localisé de la propriété. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Lecture seule<br/> | Visability de la propriété. <br/>               |
| [**Évit**](-search-2x-iresultproperty-hint.md)<br/>                 | Lecture seule<br/> | Valeur spéciale utilisée pour faciliter la récupération de données. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Lecture seule<br/> | Nom de la colonne des propriétés dans l’index. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Lecture seule<br/> | Identificateur unique de la propriété. <br/>       |



 

## <a name="remarks"></a>Remarques

Il s’agit des propriétés de retour des éléments.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

