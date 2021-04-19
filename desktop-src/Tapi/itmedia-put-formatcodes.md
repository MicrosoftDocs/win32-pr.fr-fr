---
description: La \_ méthode put FormatCodes définit la liste des codes de format de charge utile du support. Le variant contient un SAFEARRAY de BSTR. Chaque BSTR au sein de ce tableau est une chaîne de code de format.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: ITMedia ::p ut_FormatCodes, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525108"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia ::p ut \_ FormatCodes, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **put \_ FormatCodes** définit la liste des codes de format de charge utile du support. Le variant contient un SAFEARRAY de **BSTR** s. Chaque **BSTR** au sein de ce tableau est une chaîne de code de format.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewVal* \[ dans\]
</dt> <dd>

Liste des codes de format de charge utile du support.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *newVal* n’est pas valide.<br/>                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

Quand une liste de formats de charge utile est donnée, cela implique que tous ces formats peuvent être utilisés dans la session, mais que le premier de ces formats soit le format par défaut de la session. Lorsque le protocole de transport est RTP, les codes de format sont des types de charge utile RTP.

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

[**ITMedia :: obtient \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




