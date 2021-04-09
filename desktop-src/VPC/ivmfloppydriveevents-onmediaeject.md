---
title: Méthode IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été éjecté du lecteur. | Méthode IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- Méthode OnMediaEject Virtual PC
- Méthode OnMediaEject Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, méthode OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870054"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>IVMFloppyDriveEvents :: OnMediaEject, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que le média a été éjecté du lecteur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnMediaEject(
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

## <a name="remarks"></a>Notes

Cette méthode est appelée lorsque le média (une image de disquette ou une disquette dans un lecteur hôte) est éjecté. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmFloppyDriveEvent OnMediaEject provenant de [**IVMFloppyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

