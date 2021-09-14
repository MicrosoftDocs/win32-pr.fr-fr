---
description: Récupère le champ de données à partir de l’unité de données du protocole d’application (APDU), en le plaçant dans un objet de mémoire tampon d’octets.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'ISCardCmd :: get_Data, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011236"
---
# <a name="iscardcmdget_data-method"></a>ISCardCmd :: méthode d’extraction de \_ données

\[La méthode **obtenir des \_ données** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir des \_ données** récupère le champ de données à partir de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU), en le plaçant dans un objet de mémoire tampon d’octets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppData* \[ à\]
</dt> <dd>

Pointeur vers l’objet de mémoire tampon d’octets (**IStream**) qui contient le champ de données APDU au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *ppData* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppData*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                        |



 

## <a name="remarks"></a>Notes

Pour définir le champ de données du APDU, appelez [**put \_ Data**](iscardcmd-put-data.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer le champ de données de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pIByteData est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) , et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
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
</dt> <dt>

[**placer des \_ données**](iscardcmd-put-data.md)
</dt> </dl>

 

 
