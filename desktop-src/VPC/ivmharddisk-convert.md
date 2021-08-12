---
title: Méthode Convert IVMHardDisk (VPCCOMInterfaces. h)
description: Convertit un disque dur virtuel de taille fixe en disque dur virtuel de taille dynamique ou convertit un disque dur virtuel de taille dynamique en disque dur virtuel de taille fixe.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertir la méthode Virtual PC
- Méthode de conversion Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593882"
---
# <a name="ivmharddiskconvert-method"></a>IVMHardDisk :: Convert, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Convertit un disque dur virtuel de taille fixe en disque dur virtuel de taille dynamique ou convertit un disque dur virtuel de taille dynamique en disque dur virtuel de taille fixe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*convertedDiskImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès au fichier image de disque cible.

</dd> <dt>

*convertedDiskImageType* \[ dans\]
</dt> <dd>

Type de l’image de disque cible. Pour obtenir la liste des valeurs, consultez [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de conversion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'opération a réussi.<br/>                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Le paramètre *convertedDiskImagePath* est vide ou n’a pas d’extension. vhd sur le nom de fichier.<br/>                                      |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                      | Un paramètre a la **valeur null**.<br/>                                                                                                             |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl>   | Le système ne trouve pas le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* .<br/>                                                 |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>      | Le paramètre *convertedDiskImagePath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).<br/>                                    |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>      | Le paramètre *convertedDiskImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                            |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl>   | Le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* est trop long. Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt> </dl> | Soit le disque dur virtuel référencé par cet objet est en cours d’utilisation, soit le parent de ce disque dur virtuel est en cours d’utilisation.<br/>                  |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt> </dl>         | Le volume hôte ne dispose pas de suffisamment d’espace pour convertir ce disque dur virtuel.<br/>                                                        |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>    | Le fichier référencé par le paramètre *convertedDiskImagePath* existe déjà.<br/>                                                        |
| <dl> <dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt> </dl>                   | Le paramètre *convertedDiskImagePath* doit être **VmDiskType \_ dynamique** ou **vmDiskType \_ FixedSize**.<br/>                          |
| <dl> <dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt> </dl>                        | L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) ne semble pas être une image valide.<br/>          |
| <dl> <dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt> </dl>                 | Le parent du disque dur virtuel référencé par cet objet n’existe pas.<br/>                                                        |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt> </dl>                      | L’image de disque dur virtuel ne peut pas être convertie parce que l’application est en cours d’arrêt.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                              | Une erreur inattendue s’est produite.<br/>                                                                                                    |



 

## <a name="remarks"></a>Remarques

Le fichier source reste intact après le processus de conversion.

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

 

