---
description: Exécute une opération d’écriture et de lecture sur l’objet de commande de carte à puce (unité de données de protocole d’application).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard :: transaction, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 60f5be785da0cca6aac4fdf1c098d49548696420042ce60a97a46de73edde9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015559"
---
# <a name="iscardtransaction-method"></a>ISCard :: transaction, méthode

\[La méthode de **transaction** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode de **transaction** exécute une opération d’écriture et de lecture sur l’objet de commande de [*carte à puce*](../secgloss/s-gly.md) ([*unité de données de protocole d’application*](../secgloss/a-gly.md)). La chaîne de réponse de la carte à puce pour la chaîne de commande définie dans la carte qui a été envoyée à la carte à puce est accessible après le retour de cette fonction.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Pointeur vers l’objet de commande de carte à puce.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *ppCmd* n’est pas valide.<br/>           |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppCmd*.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire pour satisfaire la demande n’est pas disponible.<br/> |



 

## <a name="remarks"></a>Remarques

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’exécution d’une opération d’écriture et de lecture sur l’objet de commande de carte à puce.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**Obtient \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**Obtient \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**recevoir le \_ contexte**](iscard-get-context.md)
</dt> <dt>

[**Obtient le \_ protocole**](iscard-get-protocol.md)
</dt> <dt>

[**afficher l' \_ État**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Rattacher**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
