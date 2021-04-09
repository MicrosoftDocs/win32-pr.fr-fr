---
title: Méthode IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été éjecté du lecteur. | Méthode IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Méthode OnMediaEject Virtual PC
- Méthode OnMediaEject Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, méthode OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869734"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>IVMDVDDriveEvents :: OnMediaEject, méthode

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

Lettre de lecteur hôte, ou chemin d’accès, à l’image ISO.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est appelée lorsque le média (une image ISO ou un disque d’un lecteur hôte) est éjecté. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmDVDDriveEvent OnEject provenant de [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

