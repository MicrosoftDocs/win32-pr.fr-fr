---
title: IVMVirtualNetwork HostAdapter, propriété (VPCCOMInterfaces. h)
description: Nom de l’adaptateur auquel le réseau virtuel est connecté.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter propriété Virtual PC
- HostAdapter, propriété Virtual PC, IVMVirtualNetwork, interface
- IVMVirtualNetwork interface Virtual PC, propriété HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033117"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>IVMVirtualNetwork :: HostAdapter, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nom de l’adaptateur auquel le réseau virtuel est connecté.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom de la carte hôte à laquelle le réseau virtuel est connecté.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                            | Signification                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | L'opération a réussi.<br/>                                                                                                                              |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                 | Le paramètre a la **valeur null**.<br/>                                                                                                                                 |
| <dl> <dt>Ordinateur virtuel \_ \_Adaptateur E \_ \_ introuvable</dt> <dt>0xA0040700</dt> </dl> | La carte Ethernet hôte à laquelle ce réseau virtuel était connecté n’est plus disponible. La carte Ethernet hôte a peut-être été supprimée ou désactivée.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>         | Une erreur inattendue s’est produite.<br/>                                                                                                                          |



## <a name="remarks"></a>Notes

La carte réseau virtuelle permet à un réseau virtuel de communiquer avec des réseaux externes. Il y a généralement une carte par carte Ethernet installée sur l’ordinateur hôte. Par exemple, supposons qu’un ordinateur hôte contenait un adaptateur étiqueté « 10/100 ENET ». Pour connecter une carte réseau virtuelle au réseau attaché à « 10/100 ENET », définissez la propriété réseau **Hostadapter** du réseau virtuel sur « 10/100 ENET » et connectez la carte réseau virtuelle à ce réseau virtuel.

Si la propriété **Hostadapter** est définie sur une chaîne vide (""), la carte réseau virtuelle est connectée au réseau « réseau interne » ou au réseau « réseau partagé ». Les cartes réseau virtuelles connectées au réseau « réseau interne » n’ont pas accès aux réseaux externes sur l’hôte système. Toutefois, les cartes réseau virtuelles attachées à ce réseau virtuel peuvent toujours communiquer entre elles.

La liste complète des adaptateurs est accessible par le biais de la propriété [**IVMHostInfo :: NetworkAdapters**](ivmhostinfo-networkadapters.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

