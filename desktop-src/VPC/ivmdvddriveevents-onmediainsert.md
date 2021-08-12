---
title: Méthode IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été inséré dans le lecteur. | Méthode IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Méthode OnMediaInsert Virtual PC
- Méthode OnMediaInsert Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, méthode OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b19beabfcc4cab182af850d27d3d45ea565b266e8bcaa8fa2488aa145f43fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595733"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>IVMDVDDriveEvents :: OnMediaInsert, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que le média a été inséré dans le lecteur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mediaPath* \[ dans\]
</dt> <dd>

Lettre de lecteur hôte, ou chemin d’accès, à l’image ISO.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée lorsque le média (une image ISO ou un disque d’un lecteur hôte) est inséré. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmDVDDriveEvent OnInsert provenant de [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

