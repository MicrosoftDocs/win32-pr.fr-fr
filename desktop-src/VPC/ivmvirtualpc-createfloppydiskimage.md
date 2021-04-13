---
title: Méthode IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Crée un fichier image de disquette.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Méthode CreateFloppyDiskImage Virtual PC
- Méthode CreateFloppyDiskImage Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466263"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>IVMVirtualPC :: CreateFloppyDiskImage, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crée un fichier image de disquette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet au nouveau fichier image de disque. Le dossier conteneur sera créé s’il n’existe pas.

</dd> <dt>

*ImageType* \[ dans\]
</dt> <dd>

Type d’image de disquette à créer. Seuls les **vmFloppyDiskImage \_ LowDensity** (1) et **vmFloppyDiskImage \_ HighDensity** (2) sont pris en charge. Consultez [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                                                                         | L'opération a réussi.<br/>                                                                                                                  |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *ImagePath* a la **valeur null**.<br/>                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre *ImageType* n’est pas [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) ou **vmFloppyDiskImage \_ HighDensity** (2).<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .<br/>                                                                        |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).<br/>                                                           |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                                                   |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long. La longueur du chemin d’accès doit être inférieure à 260 caractères.<br/>                          |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>  | Le fichier référencé par le paramètre *ImagePath* existe déjà.<br/>                                                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt> </dl>       | Il n’y a pas suffisamment d’espace sur le volume hôte pour créer l’image de disquette virtuelle.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                                           |



 

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

 

