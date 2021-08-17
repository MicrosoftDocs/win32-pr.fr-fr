---
title: IVMDVDDrive HostDriveLetter, propriété (VPCCOMInterfaces. h)
description: Lettre du lecteur hôte défini pour cet appareil.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter propriété Virtual PC
- HostDriveLetter, propriété Virtual PC, IVMDVDDrive, interface
- IVMDVDDrive interface Virtual PC, propriété HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eb9105ec970331a755881d7f5b1425cf43c58f5267f5970042ce64b458070a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056867"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>IVMDVDDrive :: HostDriveLetter, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la lettre du jeu de lecteurs hôtes pour cet appareil.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valeur de la propriété

Lettre de lecteur.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                            | Signification                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | L'opération a réussi.<br/>                             |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                 | Le paramètre a la **valeur null**.<br/>                                |
| <dl> <dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                         |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>         | L’ordinateur virtuel est introuvable.<br/>                   |
| <dl> <dt>Ordinateur virtuel \_ \_Type de média E \_ incorrect \_ </dt> <dt>0xA00400728</dt> </dl> | Le support capturé par ce lecteur de DVD n’est pas un lecteur hôte.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>         | Une erreur inattendue s’est produite.<br/>                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

