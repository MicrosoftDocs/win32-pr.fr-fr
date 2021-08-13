---
title: IVMHardDisk compact, méthode (VPCCOMInterfaces. h)
description: Compacte une image de disque dur virtuel de taille dynamique.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Méthode compact PC virtuelle
- Méthode compact PC Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode compact
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2ae6c8bcb4237f98c8bcb47089294b202e3e9c45e51351c9818a08e2a295ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472163"
---
# <a name="ivmharddiskcompact-method"></a>IVMHardDisk :: compact, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Compacte une image de disque dur virtuel de taille dynamique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*compactTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de compactage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'opération a réussi.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                              | Une erreur inattendue s’est produite.<br/>                                                                                                    |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                      | Le paramètre a la **valeur null**.<br/>                                                                                                           |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt> </dl> | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est en cours d’utilisation.<br/>                                  |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt> </dl>         | Le volume hôte ne dispose pas de suffisamment d’espace pour créer un fichier temporaire nécessaire pour la compression de cette image de disque dur virtuel.<br/>     |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt> </dl>                      | L’image de disque dur virtuel ne peut pas être compactée, car l’application est en cours d’arrêt.<br/>                                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt> </dl>                         | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est marquée en lecture seule.<br/>                     |
| <dl> <dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt> </dl>                   | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) doit être un type d’image **vmDiskTypeDynamic** .<br/> |
| <dl> <dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt> </dl>                        | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) ne semble pas être une image valide.<br/>          |



 

## <a name="remarks"></a>Remarques

Pour compacter une image de disque dur de taille dynamique, l’espace libre sur l’image de disque doit d’abord être mis à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

