---
title: IVMDVDDrive, propriété de la propriété image (VPCCOMInterfaces. h)
description: Récupère le chemin d’accès complet du jeu de fichiers image pour cet appareil.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Propriété de image Virtual PC
- Propriété de image Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, propriété image
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275826aaea8dcb4f40427f2448a5edc86a992aefa4dc81648703a5f0a2948604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123754"
---
# <a name="ivmdvddriveimagefile-property"></a>IVMDVDDrive :: image, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le chemin d’accès complet du jeu de fichiers image pour cet appareil.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès complet au fichier image.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                            | Signification                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | L'opération a réussi.<br/>                                  |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                 | Le paramètre a la **valeur null**.<br/>                                     |
| <dl> <dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                              |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>         | L’ordinateur virtuel est introuvable.<br/>                        |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl>      | L’emplacement du bus pour ce lecteur n’est pas valide.<br/>                  |
| <dl> <dt>Ordinateur virtuel \_ \_Type de média E \_ incorrect \_ </dt> <dt>0xA00400728</dt> </dl> | Le support capturé par ce lecteur de DVD n’est pas un fichier image ISO.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>         | Une erreur inattendue s’est produite.<br/>                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

