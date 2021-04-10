---
title: Méthode IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Récupère le type d’un fichier image de disquette existant.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Méthode GetFloppyDiskImageType Virtual PC
- Méthode GetFloppyDiskImageType Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106042"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a>IVMVirtualPC :: GetFloppyDiskImageType, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le type d’un fichier image de disquette existant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet au fichier image de disque.

</dd> <dt>

*ImageType* \[ out, retval\]
</dt> <dd>

Type d’image de disque. Pour obtenir la liste des valeurs, consultez [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                         |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *ImagePath* ou *ImageType* a la **valeur null**.<br/>                                                                 |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt> </dl> | Le système ne peut pas trouver le fichier spécifié par le paramètre *ImagePath* .<br/>                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .<br/>                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).<br/>                                  |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                          |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long. La longueur du chemin d’accès doit être inférieure à 260 caractères.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Le fichier spécifié par *ImagePath* n’est pas une image de disquette, ou une erreur inattendue s’est produite.<br/>                         |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                  |



 

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

 

