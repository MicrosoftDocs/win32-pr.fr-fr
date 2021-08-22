---
description: Spécifie un nouvel identificateur de classe de remplacement dans l’unité de données du protocole d’application (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: ISCardCmd ::p ut_AlternateClassId, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fd1f74dee017cb72a67ecb4a9fc42da85153966336b25e54819be13464b3b7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481559"
---
# <a name="iscardcmdput_alternateclassid-method"></a>ISCardCmd ::p ut \_ AlternateClassId, méthode

\[La méthode **put \_ AlternateClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **put \_ AlternateClassId** spécifie un nouvel identificateur de classe de remplacement dans le protocole APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byClass* \[ dans\]
</dt> <dd>

Autre identificateur de classe. La valeur par défaut est zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération exécutée avec succès.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *byClass* n’est pas valide.<br/> |



 

## <a name="remarks"></a>Remarques

Avec les communications utilisant le [*protocole T = 0*](../secgloss/t-gly.md), les commandes de carte supplémentaires peuvent être générées automatiquement par le APDU et envoyées à l’unité de données de protocole de transmission (TPDU). Les commandes supplémentaires utilisent généralement le même ID de classe que la commande d’origine. la spécification d’un nouvel ID de classe au moyen de cette méthode permet aux commandes générées automatiquement d’utiliser le nouvel ID de classe.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir un nouvel identificateur de classe de remplacement dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU). L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Obtient \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
