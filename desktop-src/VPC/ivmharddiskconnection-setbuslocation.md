---
title: Méthode IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Définit l’emplacement du bus auquel ce disque dur est attaché.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Méthode SetBusLocation Virtual PC
- Méthode SetBusLocation Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC, méthode SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f2ff59b0318c321d1fb5ce75bac8c5604c5e96474c52565732ec3794b4aab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974349"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>IVMHardDiskConnection :: SetBusLocation, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’emplacement du bus auquel ce disque dur est attaché.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vmBusNumber* \[ dans\]
</dt> <dd>

Numéro de bus à utiliser.

</dd> <dt>

*vmDeviceNumber* \[ dans\]
</dt> <dd>

Numéro d’appareil à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                               | Description                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | L'opération a réussi.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | L’emplacement de bus spécifié n’est pas valide.<br/>                                                         |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt> </dl>    | Impossible de définir l’emplacement du bus, car l’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.<br/>    |
| <dl> <dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt> </dl> | Impossible de définir l’emplacement du bus, car un autre appareil est actuellement attaché à cet emplacement.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl>            | Le lecteur actuel n’est pas valide.<br/>                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>               | L’ordinateur virtuel actuel n’est pas valide.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>               | Une erreur inattendue s’est produite.<br/>                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

