---
title: IVMGuestOS HeartbeatPercentage, propriété (VPCCOMInterfaces. h)
description: Pourcentage de pulsations attendues reçues au cours de la dernière minute.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage propriété Virtual PC
- HeartbeatPercentage, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1415b9d59e28e5658dc5b54a1a6d118e0b12a77b3208978448afb2b336f313e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753446"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>IVMGuestOS :: HeartbeatPercentage, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le pourcentage de pulsations attendues reçues au cours de la dernière minute.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valeur de la propriété

Pourcentage de pulsations attendues reçues au cours de la dernière minute.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                              | Signification                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'opération a réussi.<br/>                                                                                                            |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                   | Le paramètre a la **valeur null**.<br/>                                                                                                               |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>           | La configuration est inconnue.<br/>                                                                                                            |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>      | L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.<br/>                                                                             |
| <dl> <dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt> </dl> | La machine virtuelle n’est pas entièrement démarrée, la fonctionnalité composants d’intégration n’est pas installée ou la version installée ne prend pas en charge cette fonctionnalité.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>           | Une erreur inattendue s’est produite.<br/>                                                                                                        |



## <a name="remarks"></a>Remarques

les composants d’intégration envoient une pulsation périodique à Windows Virtual PC pendant que le système d’exploitation invité est en cours d’exécution. si le système d’exploitation invité est très chargé, Windows Virtual PC recevra moins de pulsations que prévu. Si le pourcentage de pulsations chute à zéro, il est possible que le système d’exploitation invité ne réponde pas ou soit bloqué. L’ordinateur virtuel doit être en cours d’exécution (c’est-à-dire être entièrement amorcé et ne pas s’arrêter) et des composants d’intégration doivent être installés lorsque cette propriété est appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

