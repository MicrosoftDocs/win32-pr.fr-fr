---
title: Énumération VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Spécifie les événements du lecteur de DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Virtual PC de l’énumération VMDVDDriveEvent
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125e2f8f9d126e582d47376f5c23b56051d3f75d9af6493a1f273cc5be93195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751981"
---
# <a name="vmdvddriveevent-enumeration"></a>Énumération VMDVDDriveEvent

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie les événements du lecteur de DVD.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ OnInsert**
</dt> <dd>

Une image ISO est attachée ou un média réel est inséré dans un lecteur hôte.

</dd> <dt>

<span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ OnEject**
</dt> <dd>

Le support a été éjecté.

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

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

