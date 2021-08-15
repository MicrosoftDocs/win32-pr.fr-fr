---
title: Interface IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Définit une collection de lecteurs de disquettes dans l’ordinateur virtuel.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Virtual PC de l’interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653589"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interface IVMFloppyDriveCollection

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit une collection de lecteurs de disquettes dans l’ordinateur virtuel. Pour obtenir un objet **IVMFloppyDriveCollection** , utilisez la propriété [**IVMVirtualMachine :: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Membres

L’interface **IVMFloppyDriveCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMFloppyDriveCollection** possède les propriétés suivantes.



| Propriété                                                          | Type d’accès          | Description                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                |
| [**Count**](ivmfloppydrivecollection-count.md)<br/>        | Lecture seule<br/> | Nombre de lecteurs de disquette dans ce regroupement.<br/>                  |
| [**Élément**](ivmfloppydrivecollection-item.md)<br/>          | Lecture seule<br/> | Objet lecteur de disquette qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection est défini en tant que 8ba70a25-F698-4EE5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

