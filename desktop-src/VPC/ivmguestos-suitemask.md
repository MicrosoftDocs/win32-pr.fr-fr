---
title: IVMGuestOS SuiteMask, propriété (VPCCOMInterfaces. h)
description: Récupère le SuiteMask du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask propriété Virtual PC
- SuiteMask, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743589"
---
# <a name="ivmguestossuitemask-property"></a>IVMGuestOS :: SuiteMask, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le SuiteMask du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Valeur de la propriété

Masque de suite. Les valeurs de chaîne suivantes sont prises en charge.



| Valeur                                                                                   | Signification                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | Les composants Microsoft BackOffice sont installés.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition est installé.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, Compute Cluster Edition est installé.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Windows Server 2008 R2 Entreprise, Windows Server 2008 entreprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded est installé.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Bureau à distance est pris en charge, mais une seule session interactive est prise en charge.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | Services Bureau à distance est installé. Cette valeur est toujours définie.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Server famille est installé.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                           |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | La machine virtuelle n’est pas en cours d’exécution.<br/>                               |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration ne sont pas installés sur cette machine virtuelle.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

