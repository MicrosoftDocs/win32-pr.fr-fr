---
title: Méthode IVMVirtualPC CreateFixedVirtualHardDisk (VPCCOMInterfaces. h)
description: Crée un disque dur virtuel de taille fixe.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Méthode CreateFixedVirtualHardDisk Virtual PC
- Méthode CreateFixedVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateFixedVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103960"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a>IVMVirtualPC :: CreateFixedVirtualHardDisk, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crée un disque dur virtuel de taille fixe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet au nouveau fichier image de disque. Le dossier conteneur sera créé s’il n’existe pas.

</dd> <dt>

*taille* \[ dans\]
</dt> <dd>

Taille, en mégaoctets, de l’image. La taille maximale est de 2 088 960 Mo (2040GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la création de l’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Un paramètre a la **valeur null**.<br/>                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre de *taille* est inférieur ou égal à 0.<br/>                                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .<br/>                                                                              |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ lecteur non valide)**</dt> <dt>0x8007000f</dt> </dl>   | Le fichier spécifié par le paramètre *ImagePath* se trouve sur un CD-ROM ou un DVD-ROM.<br/>                                                                           |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).<br/>                                                                 |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif. Au moins l’un des paramètres doit être un chemin d’accès absolu.<br/>                         |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long. La longueur du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.<br/>                |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>  | Le fichier référencé par le paramètre *ImagePath* existe déjà.<br/>                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt> </dl>       | L’image de disque dur virtuel de taille dynamique nécessite au moins 8 Mo d’espace libre sur le volume hôte.<br/>                                                       |
| <dl> <dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ grande**</dt> <dt>0xA0040683</dt> </dl>                | La *taille* du paramètre doit être inférieure à 2 088 960 Mo. Si le format est FAT16, le paramètre de *taille* doit être inférieur à 2000 Mo.<br/>                    |
| <dl> <dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ petite**</dt> <dt>0xA0040684</dt> </dl>                | Les images de disque dur virtuel au format non formaté et FAT16 doivent avoir au moins 3 Mo. Les images de disque dur virtuel au format FAT32 doivent avoir au moins 514 Mo.<br/>    |
| <dl> <dt>**Ordinateur virtuel \_ \_Fichier E \_ trop \_ volumineux \_ pour le \_ volume**</dt> <dt>0xA0040679</dt> </dl>          | Le volume hôte ne peut pas prendre en charge un fichier de cette taille. La taille de fichier maximale pour un volume FAT32 est de 4 Go. La taille de fichier maximale pour un volume FAT16 est de 2 Go.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt> </dl>                    | Le disque dur virtuel ne peut pas être créé après l’arrêt de l’application.<br/>                                                             |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

