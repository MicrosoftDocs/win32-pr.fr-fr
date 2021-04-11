---
description: Récupère l’octet d’état de la réponse APDU SW2.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'ISCardCmd :: get_ReplyStatusSW2, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113215"
---
# <a name="iscardcmdget_replystatussw2-method"></a>ISCardCmd :: \_ ReplyStatusSW2, méthode

\[La méthode **obtenir \_ ReplyStatusSW2** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir \_ ReplyStatusSW2** récupère l’octet d’état de la [*réponse APDU*](../secgloss/r-gly.md) SW2.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbySW2* \[ à\]
</dt> <dd>

Pointeur vers l’octet qui contient la valeur de l’octet SW2 sur le retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbySW2* n’est pas valide.<br/>            |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *pbySW2*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                        |



 

## <a name="remarks"></a>Notes

L’octet d’État SW2 de la réponse APDU est en lecture seule.

Pour récupérer l’octet d’État SW1 de la réponse APDU, appelez [**obtenir \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer l’octet d’État SW2 de la [*réponse APDU*](../secgloss/r-gly.md). L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Obtient \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[**Obtient \_ ReplyStatus**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
