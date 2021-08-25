---
title: Méthode IVMFloppyDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libère une image de support de disquette sur l’ordinateur hôte à partir du lecteur de disquette.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- Méthode ReleaseImage Virtual PC
- Méthode ReleaseImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253e62ec35ccca5a254c6e70ef7fd1890fb6c1a52848c84d319686e0726a038d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654049"
---
# <a name="ivmfloppydrivereleaseimage-method"></a>IVMFloppyDrive :: ReleaseImage, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libère une image de support de disquette sur l’ordinateur hôte à partir du lecteur de disquette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                          | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'opération a réussi.<br/>                                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>          | La configuration de cette machine virtuelle n’est pas valide ou est introuvable.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt> </dl>  | Le support attaché à ce lecteur de disquette n’est pas une image de disquette.<br/>         |
| <dl> <dt>**Ordinateur virtuel \_ E \_ aucun \_ support \_ capturé**</dt> <dt>0xA00400652</dt> </dl> | Aucun support n’est attaché à ce lecteur de disquette.<br/>                            |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>          | Une erreur inattendue s’est produite.<br/>                                           |



 

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

 

