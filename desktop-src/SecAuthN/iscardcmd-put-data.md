---
description: Définit le champ de données dans l’unité de données du protocole d’application (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: ISCardCmd ::p ut_Data, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 53b32cd585e87af2884920305b8aa0ae427fa9389e3c528243c18fb548289a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481429"
---
# <a name="iscardcmdput_data-method"></a>ISCardCmd ::p \_ méthode de données ut

\[La méthode **put \_ Data** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ Data** définit le champ de données dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers l’objet de mémoire tampon d’octets (**IStream**) à copier dans le champ de données APDU.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pData* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *pData*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                       |



 

## <a name="remarks"></a>Remarques

Lorsque vous définissez une nouvelle partie des données du message, la longueur du champ de données est calculée et stockée dans le paramètre P3 du APDU. Pour récupérer la longueur du champ de données, appelez [**obtenir \_ P3**](iscardcmd-get-p3.md).

Pour récupérer le champ de données de l’APDU, appelez [**obtenir des \_ données**](iscardcmd-get-data.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir le champ de données dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pIByteData est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) , et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**récupérer des \_ données**](iscardcmd-get-data.md)
</dt> <dt>

[**Accédez à \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
