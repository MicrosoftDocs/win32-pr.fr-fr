---
description: Place un autre mot et sa position dans l’objet IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: IWordSink ::P méthode utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515416"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink ::P méthode utAltWord

Place un autre mot et sa position dans l’objet [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutAltWord(
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

Pointeur vers une mémoire tampon qui contient une autre forme d’un mot du texte source. Ce paramètre n’est pas modifié par **PutAltWord**. Vous pouvez transmettre le paramètre *pTextSource* à partir de [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , le cas échéant.

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
| <dl> <dt>**\_OK**</dt> </dl>                     | L’opération s’est terminée avec succès. Indique également qu’il ne reste plus de texte à traiter.<br/>                                            |
| <dl> <dt>**Langue \_ \_ \_ mot S grand**</dt> </dl> | La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IWordBreaker :: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Notes

**PutAltWord** place une autre forme de mot dans le [**IWordSink**](iwordsink.md). Le mot est placé à la même position que le mot d’origine dans la source de texte (*pTextSource* dans [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). Par défaut, **PutAltWord** met fin à des mots avec un type d’arrêt **WORDREP \_ break \_ EOW** à partir du type énuméré de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .

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

 

 
