---
description: Cette méthode est utilisée pour rechercher la réserve réelle avec le paramètre d’entrée correspondant au nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Méthode CalculatePossibleReserve de la classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756622"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Méthode CalculatePossibleReserve de la \_ classe ProcessorPool MSVM

Cette méthode est utilisée pour rechercher la réserve réelle avec le paramètre d’entrée correspondant au nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée. Cette méthode est nécessaire car la réservation des ressources du processeur dépend fortement du nombre de processeurs qui doivent être planifiés en parallèle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProcessorCount* \[ dans\]
</dt> <dd>

Type : **UInt16**

Nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée. La valeur maximale de cette propriété est le nombre de processeurs logiques pour l’ordinateur hôte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Quantité de ressources de processeur qui peuvent être réservées pour un ordinateur virtuel.

## <a name="remarks"></a>Notes

L’accès à la classe [**MSVM \_ ProcessorPool**](msvm-processorpool.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

