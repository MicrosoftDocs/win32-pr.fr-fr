---
description: Définit l’identificateur d’instruction donné dans le APDU (Application Protocol Data Unit).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: ISCardCmd ::p ut_InstructionId, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311350"
---
# <a name="iscardcmdput_instructionid-method"></a>ISCardCmd ::p ut \_ InstructionId, méthode

\[La méthode **put \_ InstructionId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ InstructionId** définit l’identificateur d’instruction donné dans le [*protocole APDU (Application Protocol Data Unit*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byIns* \[ dans\]
</dt> <dd>

Octet qui est l’identificateur d’instruction.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *byIns* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                      |



 

## <a name="remarks"></a>Notes

Pour récupérer l’identificateur pédagogique existant, appelez la [**\_ InstructionId**](iscardcmd-get-instructionid.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir un identificateur d’instruction dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
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

[**Obtient \_ InstructionId**](iscardcmd-get-instructionid.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
