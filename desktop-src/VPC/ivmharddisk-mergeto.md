---
title: Méthode IVMHardDisk MergeTo (VPCCOMInterfaces. h)
description: Fusionne un disque dur virtuel de différenciation avec tous ses parents.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Méthode MergeTo Virtual PC
- Méthode MergeTo Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode MergeTo
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103966"
---
# <a name="ivmharddiskmergeto-method"></a>IVMHardDisk :: MergeTo, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fusionne un disque dur virtuel de différenciation avec tous ses parents (jusqu’à et y compris le disque dur virtuel parent racine) vers un nouveau fichier de disque dur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newDiskImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès à la nouvelle image de disque cible dans laquelle les images de disque sélectionnées seront fusionnées.

</dd> <dt>

*newDiskImageType* \[ dans\]
</dt> <dd>

Type de nouvelle image de disque cible. Les types d’images autorisés pour la nouvelle image de disque cible sont **vmDiskType \_ Dynamic** et **vmDiskType \_ FixedSize**. Pour plus d’informations, consultez [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de fusion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'opération a réussi.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                      | Un paramètre a la **valeur null**.<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Le paramètre *newDiskImagePath* est vide.<br/>                                                                                                                                                                                                                                                         |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt> </dl>   | Le système ne peut pas trouver le fichier spécifié par le paramètre *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl>   | Le système ne trouve pas le chemin d’accès spécifié par le paramètre *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>      | Le paramètre *newDiskImagePath* contient un caractère non valide (l’un des éléments suivants : " \* ? <>/ \| " : ").<br/>                                                                                                                                                                                         |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>      | Le paramètre *newDiskImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                                                                                                                                                                                                |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl>   | Le chemin d’accès spécifié par le paramètre *newDiskImagePath* est trop long. Le chemin d’accès doit être inférieur à 260 caractères.<br/>                                                                                                                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt> </dl> | Soit le disque dur virtuel référencé par cet objet est en cours d’utilisation, soit le parent de ce disque dur virtuel est en cours d’utilisation.<br/>                                                                                                                                                                                |
| <dl> <dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt> </dl>                   | Cette erreur est due au fait que l’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) n’est pas une image de disque de différenciation ou que le paramètre *newDiskImageType* n’est pas l’une des valeurs acceptées, **vmDiskType \_ Dynamic** ou **vmDiskType \_ FixedSize**.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>    | Le fichier référencé par le paramètre *newDiskImagePath* existe déjà.<br/>                                                                                                                                                                                                                            |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt> </dl>         | Le volume hôte ne dispose pas de suffisamment d’espace pour fusionner ce disque dur virtuel.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt> </dl>                 | Le parent du disque dur virtuel référencé par cet objet n’existe pas.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt> </dl>                      | Impossible de fusionner l’image de disque dur virtuel, car l’application est en cours d’arrêt.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                              | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                                                                                                                  |



 

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

 

