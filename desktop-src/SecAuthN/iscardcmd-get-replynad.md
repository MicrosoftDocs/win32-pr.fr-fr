---
description: Récupère l’adresse de nœud (NAD) utilisée par la carte à puce dans le message de réponse.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'ISCardCmd :: get_ReplyNad, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011221"
---
# <a name="iscardcmdget_replynad-method"></a>ISCardCmd :: \_ ReplyNad, méthode

\[La méthode **obtenir \_ ReplyNad** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir \_ ReplyNad** récupère l’adresse de nœud (NAD) utilisée par la [*carte à puce*](../secgloss/s-gly.md) dans le message de réponse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbNad* \[ à\]
</dt> <dd>

Pointeur vers l’octet qui contient le NAD utilisé par le message de réponse, au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                    | Description                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>           | L’opération s’est terminée avec succès.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Le paramètre *pbNad* n’est pas valide.<br/>                     |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl> | Les appels internes n’ont pas pu récupérer les informations du NAD.<br/> |



 

## <a name="remarks"></a>Notes

Outre les codes d’erreur COM listés ci-dessus, cette méthode peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer l’adresse de nœud (NAD) utilisée par la [*carte à puce*](../secgloss/s-gly.md) dans le message de réponse. L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
