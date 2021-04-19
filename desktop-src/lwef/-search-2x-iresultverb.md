---
title: Interface IResultVerb (WdsSharedIDL. h)
description: Expose les propriétés de verbe.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultVerb
- Fonctionnalités d’environnement Windows héritées de l’interface IResultVerb, Description
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513615"
---
# <a name="iresultverb-interface"></a>Interface IResultVerb

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Expose les propriétés de verbe.

## <a name="members"></a>Membres

L’interface **IResultVerb** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultVerb** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IResultVerb** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès           | Description                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**NomComplet**](-search-2x-iresultverb-displayname.md)<br/> | Lecture seule<br/>  | Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe. <br/>                           |
| [**DoIt**](-search-2x-iresultverb-doit.md)<br/>               | Écriture seule<br/> | Exécute le verbe. <br/>                                                                                    |
| [**Enabled**](-search-2x-iresultverb-enabled.md)<br/>         | Lecture seule<br/>  | Cette propriété retourne la valeur TRUE si le verbe est activé. <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | Lecture seule<br/>  | Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe. <br/>                            |
| [**Icône**](-search-2x-iresultverb-icon.md)<br/>               | Lecture seule<br/>  | Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe. <br/>              |
| [**Nom**](-search-2x-iresultverb-name.md)<br/>               | Lecture seule<br/>  | Cette propriété retourne un pointeur vers le nom de cononical pour le verbe, tel que imprimer, ouvrir, et ainsi de suite. <br/> |



 

## <a name="remarks"></a>Notes

Ces méthodes exposent les propriétés et les actions applicables aux verbes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

