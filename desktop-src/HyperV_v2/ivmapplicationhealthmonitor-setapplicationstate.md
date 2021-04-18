---
description: Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'IVmApplicationHealthMonitor :: SetApplicationState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536350"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>IVmApplicationHealthMonitor :: SetApplicationState, méthode

Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

Représentation **BSTR** du **GUID** qui identifie l’application. L’application appelante est chargée de créer et de gérer les identificateurs qu’elle utilise pour les applications surveillées.

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom d’affichage de l’application. Ce nom est utilisé dans une entrée de journal des événements d’information pour le changement d’État.

</dd> <dt>

*État* \[ dans\]
</dt> <dd>

Valeur de l’énumération de l' [**\_ État**](application-state.md) de l’application qui spécifie le nouvel état d’intégrité de l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’état des applications en cours d’exécution sur l’ordinateur virtuel est reflété dans la valeur de la propriété **OperationalStatus** \[ 1 \] de la classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .

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

 

 




