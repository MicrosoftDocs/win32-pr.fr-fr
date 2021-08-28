---
description: Met une autre forme d’un mot dans l’objet IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: IWordFormSink ::P méthode utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 874428ed435d2336398f6e72c58b70de275565cce2e606f1fdddea54f0684742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944409"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink ::P méthode utAltWord

Met une autre forme d’un mot dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwcInBuf* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient une autre forme d’un mot.

</dd> <dt>

*CWC* \[ dans\]
</dt> <dd>

Nombre de caractères dans *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                              | Description                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | L’opération s’est terminée avec succès. <br/>                                                                                             |
| <dl> <dt>**Langue \_ \_ \_ mot S grand**</dt> </dl> | La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IStemmer :: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est appelée à partir de la méthode [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de l’implémentation [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Toutes les autres formes d’un mot, à l’exception de la dernière, sont placées dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) en appelant **IWordFormSink ::P utaltword**. La forme alternative finale d’un mot, qui est toujours la forme d’origine du mot, est gérée en appelant [**IWordFormSink ::P utword**](iwordformsink-putword.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rechercher. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
