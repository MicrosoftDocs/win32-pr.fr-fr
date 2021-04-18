---
title: Méthode IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Ajoute un nouveau lecteur de CD ou de DVD à la machine virtuelle.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Méthode AddDVDROMDrive Virtual PC
- Méthode AddDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512812"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>IVMVirtualMachine :: AddDVDROMDrive, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ajoute un nouveau lecteur de CD ou de DVD à la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*busNumber* \[ dans\]
</dt> <dd>

Bus auquel le lecteur sera attaché.



| Valeur                                                                        | Signification                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Le lecteur sera attaché au premier bus.<br/>  |
| <dl> <dt>1</dt> </dl> | Le lecteur sera attaché au second bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ dans\]
</dt> <dd>

Appareil auquel le lecteur sera attaché.



| Valeur                                                                        | Signification                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Le lecteur sera attaché au premier périphérique sur le bus.<br/>  |
| <dl> <dt>1</dt> </dl> | Le lecteur sera attaché au deuxième périphérique sur le bus.<br/> |



 

</dd> <dt>

*dvdDrive* \[ out, retval\]
</dt> <dd>

Objet [**IVMDVDDrive**](ivmdvddrive.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                               | Description                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | L'opération a réussi.<br/>                       |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                       | Le paramètre *dvdDrive* a la **valeur null**.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | Un paramètre n'est pas valide.<br/>                           |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>               | La configuration est inconnue.<br/>                       |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt> </dl>    | L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt> </dl> | L’emplacement de bus spécifié est en cours d’utilisation.<br/>               |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl>            | Le lecteur spécifié n’est pas valide.<br/>                   |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>               | Une erreur inattendue s’est produite.<br/>                   |



 

## <a name="remarks"></a>Notes

Vous pouvez uniquement ajouter un nouveau lecteur de CD ou de DVD à une machine virtuelle arrêtée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

