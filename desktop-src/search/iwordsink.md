---
description: Gère les mots identifiés par des césures de mots pendant la durée de l’index et la durée de la requête.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interface IWordSink (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 109a852f37f3118cd1012c7385a4f9071fdd2f8867f57036e7607c20fd2dadbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822309"
---
# <a name="iwordsink-interface"></a>Interface IWordSink

Gère les mots identifiés par des césures de mots pendant la durée de l’index et la durée de la requête.

## <a name="members"></a>Membres

L’interface **IWordSink** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordSink** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWordSink** possède ces méthodes.



| Méthode                                             | Description                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Place un autre mot et sa position dans l’objet **IWordSink** .<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Met un saut après le mot précédent.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Place un mot et sa position dans l’objet **IWordSink** .<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.<br/> |



 

## <a name="remarks"></a>Remarques

Windows La recherche crée et initialise des instances de l’objet **IWordSink** . L’objet **IWordSink** reçoit le paramètre *fQuery* pendant l’initialisation et utilise ce paramètre pour déterminer le contexte de césure des mots dans lequel l’objet est utilisé.

Les implémentations de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) reçoivent un pointeur vers l’objet **IWordSink** dans la méthode [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rechercher. h</dt> </dl> |



 

 
