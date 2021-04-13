---
title: IVMGuestOS OSPlatformId, propriété (VPCCOMInterfaces. h)
description: Identificateur de plateforme du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: c6eaba08-0407-4d22-8ed7-9660cc4879f9
keywords:
- OSPlatformId propriété Virtual PC
- OSPlatformId, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété OSPlatformId
topic_type:
- apiref
api_name:
- IVMGuestOS.OSPlatformId
- IVMGuestOS.get_OSPlatformId
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ffafc8e09c24195e5dfc7e04c3712fac2163a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465198"
---
# <a name="ivmguestososplatformid-property"></a>IVMGuestOS :: OSPlatformId, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’identificateur de plateforme du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_OSPlatformId(
  [out, retval] BSTR *platformId
);
```



## <a name="property-value"></a>Valeur de la propriété

La valeur de chaîne prise en charge est « 2 ».

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                           |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | La machine virtuelle n’est pas en cours d’exécution.<br/>                               |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration ne sont pas installés sur cette machine virtuelle.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                    |



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

 

