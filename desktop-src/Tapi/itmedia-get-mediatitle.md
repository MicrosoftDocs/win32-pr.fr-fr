---
description: La \_ méthode obtenir MediaTitle récupère un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage. Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII. Dans le cas contraire, il peut s’agir de n’importe quelle chaîne BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'ITMedia :: get_MediaTitle, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535985"
---
# <a name="itmediaget_mediatitle-method"></a>ITMedia :: \_ MediaTitle, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ MediaTitle** récupère un titre textuel pour le média que l’application peut utiliser à des fins d’information ou d’affichage. Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII. Dans le cas contraire, il peut s’agir de n’importe quelle chaîne **BSTR** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMediaTitle* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le titre du média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppMediaTitle* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMediaTitle* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia ::P ut \_ MediaTitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

