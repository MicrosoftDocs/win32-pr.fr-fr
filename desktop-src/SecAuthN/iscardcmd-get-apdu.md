---
description: Récupère l’unité de données de protocole d’application (APDU) brute.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'ISCardCmd :: get_Apdu, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034002"
---
# <a name="iscardcmdget_apdu-method"></a>ISCardCmd :: obtient la \_ méthode APDU

\[La méthode **obtenir \_ APDU** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir \_ APDU** récupère l’unité de [*données de protocole d’application*](../secgloss/a-gly.md) brute (APDU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppApdu* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon d’octets mappée via un objet **IStream** qui contient le message APDU au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *ppApdu* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppApdu*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                        |



 

## <a name="remarks"></a>Notes

Pour copier le APDU à partir d’un objet [**IByteBuffer**](ibytebuffer.md) (**IStream**) dans le APDU encapsulé dans cet objet d’interface, appelez [**put \_ APDU**](iscardcmd-put-apdu.md).

Pour déterminer la longueur des APDU, appelez [**obtenir \_ ApduLength**](iscardcmd-get-apdulength.md).

Pour obtenir la liste de toutes les méthodes fournies par l’interface [**ISCardCmd**](iscardcmd.md) , consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer l’unité de [*données de protocole d’application*](../secgloss/a-gly.md) (APDU) brute. L’exemple suppose que pISCardCmd est un pointeur valide vers l’interface [**ISCardCmd**](iscardcmd.md) , et que pIByteApdu est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
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

[**Obtient \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**placer \_ APDU**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
