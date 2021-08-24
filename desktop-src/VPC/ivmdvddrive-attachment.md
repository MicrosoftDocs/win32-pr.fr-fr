---
title: IVMDVDDrive, propriété de la pièce jointe (VPCCOMInterfaces. h)
description: Récupère le type de média attaché au lecteur de DVD dans l’ordinateur virtuel.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Propriété de pièce jointe Virtual PC
- Propriété des pièces jointes Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, propriété Attachment
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb1ef5263c428692ae41de0b1dadb25faec5b9229b37b9e33edcfbe9f922b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473229"
---
# <a name="ivmdvddriveattachment-property"></a>IVMDVDDrive :: Attachment, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le type de média attaché au lecteur de DVD dans l’ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a>Valeur de la propriété

Type de support attaché. Pour obtenir la liste des valeurs, consultez [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                       | Signification                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | L'opération a réussi.<br/>               |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>            | Le paramètre a la **valeur null**.<br/>                  |
| <dl> <dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt> </dl>               | Une erreur inattendue s’est produite.<br/>           |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>    | L’ordinateur virtuel est introuvable.<br/>     |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl> | L’emplacement du bus pour ce lecteur n’est pas valide.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>    | Une erreur inattendue s’est produite.<br/>           |



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

 

