---
title: Méthode IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libère un lecteur hôte capturé à partir du lecteur de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Méthode ReleaseHostDrive Virtual PC
- Méthode ReleaseHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384439"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>IVMDVDDrive :: ReleaseHostDrive, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libère un lecteur hôte capturé à partir du lecteur de DVD.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                         | Description                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | L'opération a réussi.<br/>                                      |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>         | L’ordinateur virtuel est introuvable.<br/>                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt> </dl> | Le support actuellement capturé n’est pas un lecteur de disque hôte.<br/>             |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl>      | Le lecteur n’a pas pu être initialisé en raison d’un emplacement de bus non valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>         | Une erreur inattendue s’est produite.<br/>                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

