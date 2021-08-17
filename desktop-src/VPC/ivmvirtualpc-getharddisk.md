---
title: Méthode IVMVirtualPC GetHardDisk (VPCCOMInterfaces. h)
description: Récupère un objet correspondant à un fichier image de disque existant.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Méthode GetHardDisk Virtual PC
- Méthode GetHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc57085662c62951032837db178888bac5cb4407b11d7777d2f165f7b9c5a100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136582"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>IVMVirtualPC :: GetHardDisk, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un objet correspondant à un fichier image de disque existant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImagePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet à un fichier image de disque existant.

</dd> <dt>

*dur* \[ out, retval\]
</dt> <dd>

Objet [**IVMHardDisk**](ivmharddisk.md) correspondant à cette image de disque.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                         |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *ImagePath* ou de la **valeur du type** *de la* valeur est null.<br/>                                                                  |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt> </dl> | Le système ne peut pas trouver le fichier spécifié par le paramètre *ImagePath* .<br/>                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .<br/>                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).<br/>                                  |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                          |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long. La longueur du chemin d’accès doit être inférieure à 260 caractères.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                     |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

