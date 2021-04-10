---
title: IVMHardDisk, méthode de fusion (VPCCOMInterfaces. h)
description: Fusionne un disque dur virtuel de différenciation avec son image de disque parent.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Méthode de fusion Virtual PC
- Méthode de fusion Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtuelle, méthode de fusion
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942322"
---
# <a name="ivmharddiskmerge-method"></a>IVMHardDisk :: Merge, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fusionne un disque dur virtuel de différenciation avec son image de disque parent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de fusion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'opération a réussi.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                      | Le paramètre a la **valeur null**.<br/>                                                                                                                                                                                             |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt> </dl> | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est en cours d’utilisation ou le parent de cette image de disque dur virtuel est en cours d’utilisation. Ou bien, ces images de disque dur peuvent faire partie d’un état enregistré.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt> </dl>                   | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) doit être une image de disque de différenciation.<br/>                                                                                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt> </dl>                         | Le parent de l’image de disque dur virtuel référencé par cet objet [**IVMHardDisk**](ivmharddisk.md) est marqué en lecture seule.<br/>                                                                                             |
| <dl> <dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt> </dl>                 | Le parent du disque dur virtuel référencé par cet objet [**IVMHardDisk**](ivmharddisk.md) n’existe pas.<br/>                                                                                                       |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt> </dl>                      | Impossible de fusionner l’image de disque dur virtuel, car l’application est en cours d’arrêt.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                              | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

