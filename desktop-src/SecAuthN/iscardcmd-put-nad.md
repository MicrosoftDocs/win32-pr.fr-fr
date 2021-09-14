---
description: Spécifie l’adresse de nœud (NAD) à utiliser avec l’interface ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: ISCardCmd ::p ut_Nad, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096382"
---
# <a name="iscardcmdput_nad-method"></a>ISCardCmd : méthode :p ut \_ nad

\[La méthode **put \_ nad** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ nad** spécifie l’adresse de nœud (NAD) à utiliser avec l’interface [**ISCardCmd**](iscardcmd.md) . Cela s’applique aux communications utilisant uniquement les communications de [*protocole T = 1*](../secgloss/t-gly.md) . Par défaut, l’objet [**ISCardCmd**](iscardcmd.md) utilise un nad de zéro.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bNad* \[ dans\]
</dt> <dd>

Octet représentant le NAD à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération s’est terminée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *bNad* n’est pas valide.<br/>    |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée uniquement lorsqu’il est nécessaire d’utiliser une valeur autre que zéro pour le NAD.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment spécifier une adresse de nœud à utiliser avec l’interface [**ISCardCmd**](iscardcmd.md) . L’exemple suppose que byNadValue est une variable de type **Byte** à laquelle une valeur a été précédemment affectée, et que pISCardCmd est un pointeur valide vers une instance de l’interface **ISCardCmd** .


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
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

 

 
