---
description: Récupère l’identificateur de classe à partir de l’unité de données de protocole d’application (APDU).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'ISCardCmd :: get_ClassId, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113230"
---
# <a name="iscardcmdget_classid-method"></a>ISCardCmd :: \_ noclassid, méthode

\[La méthode **obtenir \_ ClassID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **obtenir \_ ClassID** récupère l’identificateur de classe à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbyClass* \[ à\]
</dt> <dd>

Pointeur vers l’octet qui représente l’identificateur de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pbyClass* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *pbyClass*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                          |



 

## <a name="remarks"></a>Notes

Pour définir l’identificateur de classe sur une nouvelle valeur, appelez [**put \_ ClassID**](iscardcmd-put-classid.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer l’ID de classe. L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
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

[**put \_ ClassID**](iscardcmd-put-classid.md)
</dt> </dl>

 

 
