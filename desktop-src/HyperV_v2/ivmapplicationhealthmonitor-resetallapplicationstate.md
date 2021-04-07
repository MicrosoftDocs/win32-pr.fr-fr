---
description: Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'IVmApplicationHealthMonitor :: ResetAllApplicationState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863566"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>IVmApplicationHealthMonitor :: ResetAllApplicationState, méthode

Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle. En cas de réussite, l’état d’intégrité de toutes les applications analysées est défini sur **ApplicationStateHealthy**.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                      |
| Version<br/>                  | Composants d’intégration pour Windows 8<br/>                                                           |
| MIDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




