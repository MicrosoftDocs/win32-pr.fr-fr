---
title: IVMGuestOS IsHostTimeSyncEnabled, propriété (VPCCOMInterfaces. h)
description: Indique si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- IsHostTimeSyncEnabled propriété Virtual PC
- IsHostTimeSyncEnabled, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509325"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a>IVMGuestOS :: IsHostTimeSyncEnabled, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indique si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a>Valeur de la propriété

Utilisez la **variante \_ true** si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte et la **variante \_ false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>               |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre *IsEnabled* n’est pas spécifié.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>               |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>           |



## <a name="remarks"></a>Notes

Vous ne pouvez pas modifier ce paramètre lorsque l’ordinateur virtuel est actif (autrement dit, en cours d’exécution ou dans un état enregistré).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

