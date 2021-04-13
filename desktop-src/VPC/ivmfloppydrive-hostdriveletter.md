---
title: IVMFloppyDrive HostDriveLetter, propriété (VPCCOMInterfaces. h)
description: Lettre du lecteur hôte auquel le lecteur de disquette est attaché.
ms.assetid: 16d11e06-e3bc-4a4a-850d-f7b4122e6af9
keywords:
- HostDriveLetter propriété Virtual PC
- HostDriveLetter, propriété Virtual PC, IVMFloppyDrive, interface
- IVMFloppyDrive interface Virtual PC, propriété HostDriveLetter
topic_type:
- apiref
api_name:
- IVMFloppyDrive.HostDriveLetter
- IVMFloppyDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4896699dd3547eb3488e2fc085b5b2c54de827b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508658"
---
# <a name="ivmfloppydrivehostdriveletter-property"></a>IVMFloppyDrive :: HostDriveLetter, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la lettre du lecteur hôte auquel le lecteur de disquette est attaché.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valeur de la propriété

Lettre du lecteur de disquette physique.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                               |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                                                  |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration de cette machine virtuelle n’est pas valide ou est introuvable.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

