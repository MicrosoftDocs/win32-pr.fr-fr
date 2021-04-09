---
title: IVMNetworkAdapter EthernetAddress, propriété (VPCCOMInterfaces. h)
description: Adresse Ethernet (MAC) de l’interface réseau.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- EthernetAddress propriété Virtual PC
- EthernetAddress, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739757"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>IVMNetworkAdapter :: EthernetAddress, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit l’adresse Ethernet (MAC) de l’interface réseau.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Valeur de la propriété

Adresse MAC de la carte réseau virtuelle. Elle doit être au format "*XX* XX XX XX XX XX -  -  -  -  - *XX*", où chaque *X* est un chiffre hexadécimal.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_OK</dt> </dl>                                                                                                   | L'opération a réussi.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                              | Le paramètre a la **valeur null**.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                           | Le format du paramètre n’est pas correct.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>Ordinateur virtuel \_ E \_ Impossible de \_ définir l' \_ \_ \_ adresse MAC dynamique</dt> <dt>0xA004070A</dt> </dl> | L’adresse Ethernet pour une interface réseau peut être générée de façon dynamique ou peut être définie sur une adresse statique par l’utilisateur. Cette méthode ne peut pas être appelée lorsque l’adresse est définie pour être générée dynamiquement. La propriété [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) est utilisée pour modifier le comportement de génération de l’adresse Ethernet.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>                      | L’ordinateur virtuel est introuvable. Cela peut se produire si l’ordinateur a été supprimé après la création de l’objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                      | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

