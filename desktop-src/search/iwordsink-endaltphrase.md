---
description: Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink :: EndAltPhrase, méthode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201286"
---
# <a name="iwordsinkendaltphrase-method"></a>IWordSink :: EndAltPhrase, méthode

Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                           | Description                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_requête WBREAK \_ E \_ uniquement**</dt> </dl> | [**EndAltPhrase**](iwordsink-endaltphrase.md) est appelé pendant la durée de la requête.<br/> |



 

## <a name="remarks"></a>Notes

Les implémentations de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) appellent **IWordSink :: EndAltPhrase** à partir de la méthode [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) pour terminer une séquence d’expressions de remplacement. La méthode [**IWordSink :: StartAltPhrase**](iwordsink-startaltphrase.md) est appelée pour indiquer la fin d’une expression et le début d’une autre dans une séquence d’expressions. Seule la dernière expression d’une séquence se termine par un appel à **EndAltPhrase**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rechercher. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
