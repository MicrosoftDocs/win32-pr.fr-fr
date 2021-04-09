---
description: Définit une nouvelle réponse APDU.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: ISCardCmd ::p ut_ApduReply, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862634"
---
# <a name="iscardcmdput_apdureply-method"></a>ISCardCmd ::p ut \_ ApduReply, méthode

\[La méthode **put \_ ApduReply** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ ApduReply** définit un nouveau [*APDU de réponse*](../secgloss/r-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReplyApdu* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon d’octets (mappée via un objet **IStream** ) qui contient le message APDU de relecture au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pReplyApdu* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *pReplyApdu*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                            |



 

## <a name="remarks"></a>Notes

Pour récupérer une valeur APDU de réponse existante, appelez la [**\_ ApduReply**](iscardcmd-get-apdureply.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir une nouvelle valeur [*APDU de réponse*](../secgloss/r-gly.md). L’exemple suppose que pIByteReply est un pointeur valide vers une instance de [**IByteBuffer**](ibytebuffer.md)et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
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

[**Obtient \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**Obtient \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
