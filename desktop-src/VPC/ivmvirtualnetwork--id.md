---
title: IVMVirtualNetwork _ID, méthode (VPCCOMInterfaces. h)
description: Récupère l’identificateur interne du réseau virtuel.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c888a6191be85bf90e9bee2d83590352c3acbf4f731e835fb5879221831b0669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122659"
---
# <a name="ivmvirtualnetwork_id-method"></a>IVMVirtualNetwork :: \_ ID, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’identificateur interne du réseau virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*virtualNetworkID* \[ à\]
</dt> <dd>

Identificateur du réseau virtuel. L’identificateur du réseau virtuel de réseau partagé (NAT) est 01010101010101010101010101010101.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



 

## <a name="remarks"></a>Remarques

Cette propriété n’est pas utilisable par les langages de script.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

