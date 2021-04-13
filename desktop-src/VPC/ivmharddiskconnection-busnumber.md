---
title: IVMHardDiskConnection BusNumber, propriété (VPCCOMInterfaces. h)
description: Récupère le numéro de bus auquel l’image de lecteur est attachée.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- BusNumber propriété Virtual PC
- BusNumber, propriété Virtual PC, IVMHardDiskConnection, interface
- IVMHardDiskConnection interface Virtual PC, propriété BusNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466158"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a>IVMHardDiskConnection :: BusNumber, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le numéro de bus auquel l’image de lecteur est attachée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de bus qui correspond à cette connexion.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                       | Signification                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | L'opération a réussi.<br/>                                           |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>            | Le paramètre a la **valeur null** ou n’est pas valide.<br/>                                 |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>    | La configuration actuelle de l’ordinateur virtuel n’est pas valide.<br/>                 |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl> | L’emplacement du bus pour cette connexion n’a pas été correctement initialisé.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>    | Une erreur inattendue s’est produite.<br/>                                       |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

