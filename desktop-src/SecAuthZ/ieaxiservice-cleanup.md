---
description: Libère les ressources utilisées par l’interface IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'IeAxiService :: Cleanup, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: de0413c39a4abf47a24913f347ceed0158d0b51aa4e1da0b3005cace1326b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908379"
---
# <a name="ieaxiservicecleanup-method"></a>IeAxiService :: Cleanup, méthode

La méthode **Cleanup** libère les ressources utilisées par l’interface [**IeAxiService**](ieaxiservice.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

