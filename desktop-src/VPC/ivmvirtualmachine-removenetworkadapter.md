---
title: Méthode IVMVirtualMachine RemoveNetworkAdapter (VPCCOMInterfaces. h)
description: Supprime une interface réseau de la machine virtuelle.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Méthode RemoveNetworkAdapter Virtual PC
- Méthode RemoveNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466395"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a>IVMVirtualMachine :: RemoveNetworkAdapter, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Supprime une interface réseau de la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

Carte réseau  \[ dans\]
</dt> <dd>

Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui représente la carte réseau à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                            | Description                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'opération a réussi.<br/>                       |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                    | Le paramètre a la **valeur null**.<br/>                          |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>            | La configuration est inconnue.<br/>                       |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt> </dl> | L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>            | Une erreur inattendue s’est produite.<br/>                   |



 

## <a name="remarks"></a>Notes

Vous pouvez uniquement supprimer une interface réseau existante d’un ordinateur virtuel qui est arrêté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

