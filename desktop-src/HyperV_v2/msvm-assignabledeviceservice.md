---
description: Gère les appareils attribuables sur un système d’ordinateur hôte.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525745"
---
# <a name="msvm_assignabledeviceservice-class"></a>MSVM \_ AssignableDeviceService, classe

Gère les appareils attribuables sur un système d’ordinateur hôte.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ AssignableDeviceService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ AssignableDeviceService** possède ces méthodes.



| Méthode                                                                                    | Description                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**DismountAssignableDevice**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Démonte l’appareil PCI spécifié afin qu’il puisse être attribué.<br/>                      |
| [**MountAssignableDevice**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




