---
title: Interface IVMSerialPort (VPCCOMInterfaces. h)
description: Définit un port série à l’intérieur d’une machine virtuelle.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Virtual PC de l’interface IVMSerialPort
- IVMSerialPort interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385f22caf7b843a91987eea01a7713544475c24be741bbb56d59610cb2cd521d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752823"
---
# <a name="ivmserialport-interface"></a>Interface IVMSerialPort

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit un port série à l’intérieur d’une machine virtuelle. Cette interface vous permet de configurer des ports série à l’intérieur d’une machine virtuelle. Vous pouvez récupérer un objet **IVMSerialPort** à partir de l’objet [**IVMSerialPortCollection**](ivmserialportcollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membres

L’interface **IVMSerialPort** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPort** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMSerialPort** possède ces méthodes.



| Méthode                                       | Description                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_ID**](ivmserialport--id.md)            | Récupère l’identificateur interne du port série.<br/> |
| [**Configurer**](ivmserialport-configure.md) | Configure le port série.<br/>                           |



 

### <a name="properties"></a>Propriétés

L’interface **IVMSerialPort** possède les propriétés suivantes.



| Propriété                                                                  | Type d’accès          | Description                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Lecture seule<br/> | Indique si le port série doit être ouvert sans attendre la réception d’une commande de modem.<br/> |
| [**Nom**](ivmserialport-name.md)<br/>                             | Lecture seule<br/> | Nom du port série.<br/>                                                                           |
| [**Type**](ivmserialport-type.md)<br/>                             | Lecture seule<br/> | Type du port série.<br/>                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815<br/>              |



 

