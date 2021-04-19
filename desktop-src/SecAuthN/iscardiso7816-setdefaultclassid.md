---
description: La méthode SetDefaultClassId affecte un octet d’identificateur de classe standard qui sera utilisé dans toutes les opérations lors de la construction d’une unité de données de protocole d’application (APDU) de commande ISO 7816-4. Par défaut, l’octet de l’identificateur de classe standard est 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816 :: SetDefaultClassId, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530582"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>ISCardISO7816 :: SetDefaultClassId, méthode

\[La méthode **SetDefaultClassId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **SetDefaultClassId** affecte un octet d’identificateur de classe standard qui sera utilisé dans toutes les opérations lors de la construction d’une [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU) de commande ISO 7816-4. Par défaut, l’octet de l’identificateur de classe standard est 0x00.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byClass* \[ dans\]
</dt> <dd>

Octet de l’ID de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                          | Description                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Opération exécutée avec succès.<br/> |



 

Pour obtenir la liste de toutes les méthodes fournies par l’interface [**ISCardISO7816**](iscardiso7816.md) , consultez **ISCardISO7816**.

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
