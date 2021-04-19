---
title: IVMHardDiskConnectionCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet de connexion de disque dur qui correspond à l’index spécifié.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMHardDiskConnectionCollection
- IVMHardDiskConnectionCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106541162"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>IVMHardDiskConnectionCollection :: Item, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’objet de connexion de disque dur qui correspond à l’index spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi. <br/>                                                      |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre *hardDiskConnection* a la **valeur null**. <br/>                                    |
| <dl> <dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L’index de l’élément demandé ne correspond pas à un élément de cette collection. <br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                               |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                      |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

