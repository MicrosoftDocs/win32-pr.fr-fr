---
description: Place le formulaire Word d’origine dans l’objet IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: IWordFormSink ::P méthode utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514791"
---
# <a name="iwordformsinkputword-method"></a>IWordFormSink ::P méthode utWord

Place le formulaire Word d’origine dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwcInBuf* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la forme alternative finale d’un mot, qui est toujours le mot d’origine.

</dd> <dt>

*CWC* \[ dans\]
</dt> <dd>

Nombre de caractères dans *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | L’opération s’est terminée avec succès. <br/> |



 

## <a name="remarks"></a>Notes

**PutWord** est appelé à partir de la méthode [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de l’implémentation [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Cette méthode gère la forme d’origine d’un mot et est appelée en dernier. Toutes les autres formes précédentes pour un mot sont placées dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) en appelant [**IWordFormSink ::P utaltword**](iwordformsink-putphrase.md).

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

 

 
