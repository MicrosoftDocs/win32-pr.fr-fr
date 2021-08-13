---
title: Méthode IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été inséré dans le lecteur. | Méthode IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Méthode OnMediaInsert Virtual PC
- Méthode OnMediaInsert Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, méthode OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30eb00222304168b30f6512b51f9d381fc4fbd61e7c5d254e0d53c3eb931a819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594778"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>IVMFloppyDriveEvents :: OnMediaInsert, méthode

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

Lettre de lecteur hôte ou chemin d’accès à l’image de disquette.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée lors de l’insertion d’un média (une image de disquette ou une disquette dans un lecteur hôte). Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmFloppyDriveEvent OnMediaInsert provenant de [**IVMFloppyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

