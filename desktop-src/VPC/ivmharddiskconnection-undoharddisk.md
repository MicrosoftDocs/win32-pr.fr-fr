---
title: IVMHardDiskConnection UndoHardDisk, propriété (VPCCOMInterfaces. h)
description: Récupère un objet disque dur correspondant à l’image de disque d’annulation de cette connexion.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk propriété Virtual PC
- UndoHardDisk, propriété Virtual PC, IVMHardDiskConnection, interface
- IVMHardDiskConnection interface Virtual PC, propriété UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102820"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>IVMHardDiskConnection :: UndoHardDisk, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un objet disque dur correspondant à l’image de disque d’annulation de cette connexion.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMHardDisk**](ivmharddisk.md) qui décrit le disque dur d’annulation associé à cette connexion.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                    |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null** ou n’est pas valide.<br/>                                                                                          |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le disque d’annulation pour cette connexion est introuvable.<br/>                                                                                 |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>                            | La configuration actuelle de l’ordinateur virtuel n’est pas valide.<br/>                                                                          |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl>                         | L’emplacement du bus pour cette connexion n’a pas été correctement initialisé, ou l’appareil à cet emplacement n’est pas un disque dur valide.<br/> |



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

 

