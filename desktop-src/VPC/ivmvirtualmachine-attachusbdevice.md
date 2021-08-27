---
title: Méthode IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Attache un périphérique USB à une machine virtuelle.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Méthode AttachUSBDevice Virtual PC
- Méthode AttachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006899"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>IVMVirtualMachine :: AttachUSBDevice, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache un périphérique USB à une machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inUSBDevice* \[ dans\]
</dt> <dd>

Pointeur [**IVMUSBDevice**](ivmusbdevice.md) qui représente le périphérique USB connecté à l’hôte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                             | Description                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | L'opération a réussi.<br/>                                           |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                     | Le paramètre a la **valeur null**.<br/>                                              |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                        | La machine virtuelle n’est pas en cours d’exécution.<br/>                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                             | La configuration est inconnue.<br/>                                           |
| <dl> <dt>**Ordinateur virtuel \_ \_Ajouts \_ non \_**</dt> réalisés <dt>0xA0040504</dt> </dl>                   | Les composants d’intégration ne sont pas disponibles dans le système d’exploitation invité.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl>          | La fonctionnalité USB n’est pas disponible.<br/>                                       |
| <dl> <dt>**Ordinateur virtuel \_ \_Erreur de \_ \_ pilote de \_ connecteur USB E**</dt> <dt>0xA00400925</dt> </dl>          | Une erreur de pilote de connecteur USB s’est produite.<br/>                                 |
| <dl> <dt>**Ordinateur virtuel \_ Échec de l' \_ attachement USB E- \_ \_ \_ \_ périphériques supplémentaires**</dt> <dt>0xA00400931</dt> </dl>     | Impossible d’attacher d’autres appareils à la machine virtuelle.<br/>                                   |
| <dl> <dt>**Ordinateur virtuel \_ Échec de l' \_ \_ \_ \_ \_ erreur de stratégie**</dt> de <dt>0xA00400932</dt> d’attachement USB </dl>         | Un paramètre de stratégie de groupe empêche la redirection USB.<br/>               |
| <dl> <dt>**Ordinateur virtuel \_ Échec de l' \_ attachement USB E 0xA00400933 \_ \_ \_ déjà \_ affecté**</dt> <dt></dt> </dl> | Un périphérique USB a déjà été attaché par un autre client.<br/>            |
| <dl> <dt>**Ordinateur virtuel \_ Échec de l' \_ \_ attachement \_ USB E**</dt> <dt>0xA00400926</dt> </dl>                    | Échec de l’opération d’attachement.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                             | Une erreur inattendue s’est produite.<br/>                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

