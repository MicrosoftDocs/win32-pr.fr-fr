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
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508986"
---
# <a name="ivmserialport-interface"></a>Interface IVMSerialPort

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit un port série à l’intérieur d’une machine virtuelle. Cette interface vous permet de configurer des ports série à l’intérieur d’une machine virtuelle. Vous pouvez récupérer un objet **IVMSerialPort** à partir de l’objet [**IVMSerialPortCollection**](ivmserialportcollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membres

L’interface **IVMSerialPort** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPort** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMSerialPort** possède ces méthodes.



| Méthode                                       | Description                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_IDENTIFI**](ivmserialport--id.md)            | Récupère l’identificateur interne du port série.<br/> |
| [**Configurer**](ivmserialport-configure.md) | Configure le port série.<br/>                           |



 

### <a name="properties"></a>Propriétés

L’interface **IVMSerialPort** possède les propriétés suivantes.



| Propriété                                                                  | Type d’accès          | Description                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Lecture seule<br/> | Indique si le port série doit être ouvert sans attendre la réception d’une commande de modem.<br/> |
| [**Nom**](ivmserialport-name.md)<br/>                             | Lecture seule<br/> | Nom du port série.<br/>                                                                           |
| [**Entrer**](ivmserialport-type.md)<br/>                             | Lecture seule<br/> | Type du port série.<br/>                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815<br/>              |



 

