---
title: Interface ISearchResult (WdsSharedIDL. h)
description: Expose des informations et des propriétés concernant le jeu de résultats.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- fonctionnalités d’environnement Windows héritées de l’interface ISearchResult
- fonctionnalités d’environnement Windows héritées de l’interface ISearchResult, description
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd15db1340b28c8ac273746a64a5aee8c4b3235155d948692ffcc16582ac4549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963519"
---
# <a name="isearchresult-interface"></a>Interface ISearchResult

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Expose des informations et des propriétés concernant le jeu de résultats.

## <a name="members"></a>Membres

L’interface **ISearchResult** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISearchResult** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISearchResult** possède ces méthodes.



| Méthode                                                            | Description                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Disponibilité**](-search-2x-isearchresult-availability.md)     | Non implémenté.<br/> |
| [**Verbe**](-search-2x-isearchresult-doverb.md)                 | Non implémenté.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Non implémenté.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Non implémenté.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Non implémenté.<br/> |
| [**GetVerb**](-search-2x-isearchresult-getverb.md)               | Non implémenté.<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | Non implémenté.<br/> |
| [**Évaluer**](-search-2x-isearchresult-index.md)                   | Non implémenté.<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | Non implémenté.<br/> |
| [**Générateur d’aperçu**](-search-2x-isearchresult-previewer.md)           | Non implémenté.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Non implémenté.<br/> |
| [**ThumbnailState**](-search-2x-isearchresult-thumbnailstate.md) | Non implémenté.<br/> |
| [**Type**](-search-2x-isearchresult-type.md)                     | Non implémenté.<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | Non implémenté.<br/> |



 

## <a name="remarks"></a>Remarques

Ces méthodes exposent les propriétés et les actions applicables au jeu de résultats.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

