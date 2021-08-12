---
title: Méthode IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Méthode AttachHostDrive Virtual PC
- Méthode AttachHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bfdfecc106acd216da5d39e7625f1fbbd9d76190eecc4c2d428595abc9e775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595723"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a>IVMFloppyDrive :: AttachHostDrive, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

lettre de *lecteur* \[ dans\]
</dt> <dd>

La lettre de lecteur du lecteur de disquette physique sur l’ordinateur hôte doit être attachée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | Le paramètre *driveLetter* a la **valeur null**, n’est pas un lecteur de disquette valide ou le chemin d’accès spécifié est vide.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration de cette machine virtuelle n’est pas valide ou est introuvable.<br/>                       |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                                                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

