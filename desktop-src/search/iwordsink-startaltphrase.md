---
description: Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink :: StartAltPhrase, méthode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412615"
---
# <a name="iwordsinkstartaltphrase-method"></a>IWordSink :: StartAltPhrase, méthode

Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                           | Description                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_requête WBREAK \_ E \_ uniquement**</dt> </dl> | [**StartAltPhrase**](iwordsink-startaltphrase.md) est appelé pendant la durée de la requête.<br/> |



 

## <a name="remarks"></a>Notes

Chaque expression de remplacement commence par un appel **StartAltPhrase** . L’expression est placée dans l’objet [**IWordSink**](iwordsink.md) via les appels suivants à la méthode [**IWordSink ::P utword**](iwordsink-putword.md) ou [**IWordSink ::P utaltword**](iwordsink-putaltword.md) . L’expression alternative finale dans une séquence d’expressions se termine par un appel à la méthode [**IWordSink :: EndAltPhrase**](iwordsink-endaltphrase.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rechercher. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 




