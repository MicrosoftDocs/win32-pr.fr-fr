---
title: Énumération VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Spécifie ce qui est attaché à un lecteur de DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Virtual PC de l’énumération VMDVDDriveAttachmentType
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e0af9397153333a8b80f2af5f2b955555fc368048d3b947ae99722e42fc11eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124639"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a>Énumération VMDVDDriveAttachmentType

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie ce qui est attaché à un lecteur de DVD.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ aucun**
</dt> <dd>

Aucun élément n’est attaché.

</dd> <dt>

<span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**\_image vmDVDDrive**
</dt> <dd>

Un fichier image ISO est attaché.

</dd> <dt>

<span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive \_ HostDrive**
</dt> <dd>

Un lecteur de CD ou de DVD hôte est attaché.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive :: Attachment**](ivmdvddrive-attachment.md)
</dt> </dl>

 

