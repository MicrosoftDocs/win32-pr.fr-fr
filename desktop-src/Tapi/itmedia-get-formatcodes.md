---
description: La \_ méthode obtenir FormatCodes obtient la liste des codes de format de charge utile du média. La variante retourne un SAFEARRAY de BSTR. Chaque BSTR au sein de ce tableau est une chaîne de code de format.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITMedia :: get_FormatCodes, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a785bd4a5a4e45bf7a6be5e1c4cb68ee8125b28aa5808c19393f8be24df7a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774909"
---
# <a name="itmediaget_formatcodes-method"></a>ITMedia :: \_ FormatCodes, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ FormatCodes** obtient la liste des codes de format de charge utile du média. La variante retourne un SAFEARRAY de **BSTR** s. Chaque **BSTR** au sein de ce tableau est une chaîne de code de format.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ à\]
</dt> <dd>

Tableau de codes de format de charge utile de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pval* n’est pas un pointeur valide.<br/>         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

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

[**ITMedia ::p ut \_ FormatCodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




