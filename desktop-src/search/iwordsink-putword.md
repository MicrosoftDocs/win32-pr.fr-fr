---
description: Place un mot et sa position dans l’objet IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: IWordSink ::P méthode utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e860aafbef633e226933281aaaa0be5c6429387542e7c3ae2d65d3026fd7fe37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597599"
---
# <a name="iwordsinkputword-method"></a>IWordSink ::P méthode utWord

Place un mot et sa position dans l’objet [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CWC* \[ dans\]
</dt> <dd>

Nombre de caractères dans *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient une autre forme d’un mot du texte source. Ce paramètre n’est pas modifié par **PutWord**. Vous pouvez transmettre le paramètre *pTextSource* à partir de [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , le cas échéant.

</dd> <dt>

*cwcSrcLen* \[ dans\]
</dt> <dd>

Nombre de caractères dans la mémoire tampon de texte source (indiqué par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) qui correspond au mot contenu dans *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ dans\]
</dt> <dd>

Position de départ du mot dans *pwcInBuf* dans la mémoire tampon de texte source (indiquée par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                              | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | L’opération s’est terminée avec succès. Indique également qu’il n’y a plus de texte disponible pour remplir la mémoire tampon.<br/>                                  |
| <dl> <dt>**Langue \_ \_ \_ mot S grand**</dt> </dl> | La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IWordBreaker :: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Remarques

Nous recommandons que la méthode **IWordSink ::P utword** contienne toujours le mot d’origine tel qu’il figure dans *pTextSource*. Les autres formes du mot sont passées à WordSink à l’aide de [**IWordSink ::P utaltword**](iwordsink-putaltword.md). Nous vous recommandons également de faire en sorte que les mots de *pwcInBuf* correspondent le mieux possible au texte source. Par exemple, conservez les majuscules et les accents lorsque cela est possible.

Cet appel doit être effectué pour chaque mot récupéré à partir de *pTextSource* , à l’exception de ceux pour lesquels l’appel [**IWordSink ::P utaltword**](iwordsink-putaltword.md) a été effectué. Le mot se termine par un caractère EOW lorsqu’il est enregistré dans le WordSink.

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

 

 
