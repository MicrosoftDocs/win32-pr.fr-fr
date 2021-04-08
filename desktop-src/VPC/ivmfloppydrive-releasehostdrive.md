---
title: Méthode IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Méthode ReleaseHostDrive Virtual PC
- Méthode ReleaseHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739772"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>IVMFloppyDrive :: ReleaseHostDrive, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                          | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'opération a réussi.<br/>                                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>          | La configuration de cette machine virtuelle n’est pas valide ou est introuvable.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt> </dl>  | Le support attaché à ce lecteur de disquette n’est pas un lecteur de disquette physique.<br/>     |
| <dl> <dt>**Ordinateur virtuel \_ E \_ aucun \_ support \_ capturé**</dt> <dt>0xA00400652</dt> </dl> | Aucun support n’est attaché à ce lecteur de disquette.<br/>                            |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>          | Une erreur inattendue s’est produite.<br/>                                           |



 

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

 

