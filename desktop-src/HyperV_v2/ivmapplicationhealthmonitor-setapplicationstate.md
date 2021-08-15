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
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392354"
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

## <a name="remarks"></a>Remarques

L’état des applications en cours d’exécution sur l’ordinateur virtuel est reflété dans la valeur de la propriété **OperationalStatus** \[ 1 \] de la classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .

pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                      |
| Version<br/>                  | Composants d’intégration pour Windows 8<br/>                                                           |
| MIDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




