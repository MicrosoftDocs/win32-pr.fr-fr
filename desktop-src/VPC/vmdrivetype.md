---
title: Énumération VMDriveType (VPCCOMInterfaces. h)
description: Spécifie le type de lecteur attaché à un emplacement de bus.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Virtual PC de l’énumération VMDriveType
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5288988ff481bb785c4478bbd0ab8d5bf96e14d06ed016bdc9f9e593a677fc12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394319"
---
# <a name="vmdrivetype-enumeration"></a>Énumération VMDriveType

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie le type de lecteur attaché à un emplacement de bus.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ null**
</dt> <dd>

Aucun lecteur n’est attaché.

</dd> <dt>

<span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType \_**
</dt> <dd>

Un disque dur est attaché.

</dd> <dt>

<span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**\_DVD vmDriveType**
</dt> <dd>

Un lecteur de CD ou DVD est attaché.

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

[**IVMVirtualMachine::AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

