---
title: Méthode IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette de la machine virtuelle.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Méthode AttachImage Virtual PC
- Méthode AttachImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595713"
---
# <a name="ivmfloppydriveattachimage-method"></a>IVMFloppyDrive :: AttachImage, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette de la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mediaImagePath* \[ dans\]
</dt> <dd>

Le chemin d’accès complet à l’image de support de disquette à attacher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre *mediaImagePath* n’est pas valide.<br/>                                                                                 |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                                                                   |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>      | La mémoire disponible est insuffisante pour effectuer cette requête.<br/>                                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *mediaImagePath* est trop long. Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *mediaImagePath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).<br/>                                    |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *mediaImagePath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                            | La configuration de cette machine virtuelle n’est pas valide ou est introuvable.<br/>                                                  |
| <dl> <dt>**Ordinateur virtuel \_ Échec de la \_ \_ capture \_ d’image E**</dt> <dt>0xA00400650</dt> </dl>                  | Impossible de capturer le fichier image spécifié.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

