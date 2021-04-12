---
title: Méthode IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Attache une image ISO au lecteur de DVD au sein de la machine virtuelle.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Méthode AttachImage Virtual PC
- Méthode AttachImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385151"
---
# <a name="ivmdvddriveattachimage-method"></a>IVMDVDDrive :: AttachImage, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache une image ISO au lecteur de DVD au sein de la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet à l’image ISO à attacher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                    | Description                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | L'opération a réussi.<br/>                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | Le paramètre *ImagePath* est un répertoire.<br/>                                                         |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>            | Le paramètre *ImagePath* a la **valeur null**.<br/>                                                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>    | La machine virtuelle est introuvable.<br/>                                                                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Lecteur E \_ en cours d' \_ utilisation**</dt> <dt>0xA0040727</dt> </dl> | Une image ISO ou un lecteur de DVD hôte est déjà attachée à ce lecteur.<br/>                                  |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl> | L’emplacement du bus pour ce lecteur n’est pas valide, ou le lecteur ne semble pas être un lecteur de DVD valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>    | Une erreur inattendue s’est produite.<br/>                                                                 |



 

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

 

