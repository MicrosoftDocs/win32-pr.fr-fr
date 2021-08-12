---
title: Méthode IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Attache l’interface réseau au réseau virtuel spécifié.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Méthode AttachToVirtualNetwork Virtual PC
- Méthode AttachToVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, méthode AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03bf8bd0bcde6ba0353ce62e227c100a17ed1df0b2267ad54cd127c95c5836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593227"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>IVMNetworkAdapter :: AttachToVirtualNetwork, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache l’interface réseau au réseau virtuel spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*virtualNetwork* \[ dans\]
</dt> <dd>

Le réseau virtuel auquel cette carte d’interface réseau virtuelle sera connectée. Consultez [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                          | Description                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                                                                       | L'opération a réussi.<br/>                           |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                  | Le paramètre a la **valeur null**.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | Le paramètre ne contient pas de réseau virtuel valide.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt> </dl> | L’accès a été refusé au réseau virtuel demandé.<br/>     |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                          | L’ordinateur virtuel n’est pas valide ou n’existe plus.<br/>     |
| <dl> <dt>**\_ID de \_ réseau virtuel non valide de \_ la machine \_ virtuelle \_**</dt> </dl>                                                                        | Le paramètre n’est pas un réseau virtuel existant.<br/>       |
| <dl> <dt>**\_exception DISP E \_**</dt> </dl>                                                                                          | Une erreur inattendue s’est produite.<br/>                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

