---
title: IVMGuestOS IntegrationComponentsVersion, propriété (VPCCOMInterfaces. h)
description: Récupère la version des composants d’intégration installés dans le système d’exploitation invité.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion propriété Virtual PC
- IntegrationComponentsVersion, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999049"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>IVMGuestOS :: IntegrationComponentsVersion, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la version des composants d’intégration installés dans le système d’exploitation invité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>Valeur de la propriété

Version.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                              | Signification                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'opération a réussi.<br/>                                                     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                   | Le paramètre a la **valeur null**.<br/>                                                        |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>           | Impossible de trouver la machine virtuelle.<br/>                                      |
| <dl> <dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt> </dl> | Les composants d’intégration ne sont pas installés sur cette machine virtuelle ou la machine virtuelle n’a jamais été démarrée.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>           | Une erreur inattendue s’est produite.<br/>                                                 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

