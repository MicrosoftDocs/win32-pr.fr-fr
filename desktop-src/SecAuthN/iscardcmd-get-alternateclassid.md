---
description: Récupère la valeur de l’ID de classe de substitution.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'ISCardCmd :: get_AlternateClassId, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542974"
---
# <a name="iscardcmdget_alternateclassid-method"></a>ISCardCmd :: \_ AlternateClassId, méthode

\[La méthode **obtenir \_ AlternateClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir \_ AlternateClassId** récupère la valeur de l’ID de classe de substitution. Cette méthode échouera à moins que l’ID de remplacement ait été défini par un appel précédent à [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbyClass* \[ à\]
</dt> <dd>

Pointeur désignant l’octet qui contient la valeur d’ID de classe de remplacement au retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne les valeurs possibles suivantes.



| Code de retour                                                                                    | Description                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>           | L’opération s’est terminée avec succès.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Le paramètre *pbyClass* n’est pas valide.<br/>                                                                                           |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl> | L’ID de classe de remplacement n’a pas été précédemment défini par un appel à [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode s’applique aux communications utilisant le [*protocole T = 0*](../secgloss/t-gly.md). Pour plus d’informations, consultez [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer l’ID de classe de substitution. L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
