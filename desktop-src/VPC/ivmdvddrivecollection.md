---
title: Interface IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Définit la collection de lecteurs de CD et de DVD dans l’ordinateur virtuel. Pour obtenir un objet IVMDVDDriveCollection, utilisez la propriété DVDROMDrives IVMVirtualMachine.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Virtual PC de l’interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77225134a88ff2c66be3f53f5d3d44c9f8353d8f44077fb0862f0c943c5aec3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056857"
---
# <a name="ivmdvddrivecollection-interface"></a>Interface IVMDVDDriveCollection

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection de lecteurs de CD et de DVD dans l’ordinateur virtuel. Pour obtenir un objet **IVMDVDDriveCollection** , utilisez la propriété [**IVMVirtualMachine ::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Membres

L’interface **IVMDVDDriveCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMDVDDriveCollection** possède les propriétés suivantes.



| Propriété                                                       | Type d’accès          | Description                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                   |
| [**Count**](ivmdvddrivecollection-count.md)<br/>        | Lecture seule<br/> | Nombre de lecteurs de CD et de DVD dans ce regroupement.<br/>                 |
| [**Élément**](ivmdvddrivecollection-item.md)<br/>          | Lecture seule<br/> | Objet lecteur de CD ou de DVD qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine ::D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

