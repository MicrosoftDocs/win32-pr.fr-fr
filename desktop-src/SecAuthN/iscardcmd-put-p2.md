---
description: Définit le deuxième octet de paramètre (P2) dans l’unité de données de protocole d’application (APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: ISCardCmd ::p ut_P2, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a66ef756d65e4cc011e6a5e4797a8ccae690dd404b6f25f1f9a7d3bbb2826069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014579"
---
# <a name="iscardcmdput_p2-method"></a>ISCardCmd ::p ut \_ P2, méthode

\[La méthode **put \_ P2** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ P2** définit le deuxième octet de paramètre (P2) dans l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byP2* \[ dans\]
</dt> <dd>

Octet qui est le champ P2.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *byP2* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                     |



 

## <a name="remarks"></a>Remarques

Pour définir la valeur P1 du APDU, appelez [**put \_ P1**](iscardcmd-put-p1.md).

Pour récupérer les valeurs P1, P2 et P3 existantes, appelez [**obtenir \_ P1**](iscardcmd-get-p1.md), [**obtenir \_ P2**](iscardcmd-get-p2.md) ou [**obtenir \_ P3**](iscardcmd-get-p3.md) , respectivement.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir le deuxième octet de paramètre (P2) de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
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

[**recevoir \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**Télécharger \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**Accédez à \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**placer \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
