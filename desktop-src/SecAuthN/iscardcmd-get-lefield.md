---
description: Retourne le champ le de l’unité de données de protocole d’application (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'ISCardCmd :: get_LeField, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011231"
---
# <a name="iscardcmdget_lefield-method"></a>ISCardCmd :: \_ LeField, méthode

\[La méthode **obtenir \_ LeField** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode d' **extraction \_ LeField** retourne le champ le de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plSize* \[ à\]
</dt> <dd>

Pointeur vers la valeur du champ le au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération s’est terminée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *plSize* n’est pas valide.<br/>  |



 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer la valeur du champ le à partir de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
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

 

 
