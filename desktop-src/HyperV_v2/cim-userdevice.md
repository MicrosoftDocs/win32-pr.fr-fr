---
description: Représente un périphérique logique qui permet à un utilisateur d’entrer, d’afficher ou d’entendre des données sur le système informatique.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Classe CIM_UserDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbd5e96c7d00574848c43fe57695ba84e39dd2c0591483a65a1f56af94cca8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068659"
---
# <a name="cim_userdevice-class-hyper-v-management"></a>Classe CIM_UserDevice (gestion Hyper-V)

Représente un périphérique logique qui permet à un utilisateur d’entrer, d’afficher ou d’entendre des données sur le système informatique.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ UserDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ UserDevice** possède les propriétés suivantes.

<dl> <dt>

**IsLocked**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si l’appareil est verrouillé, empêchant l’entrée ou la sortie de l’utilisateur ; Sinon, **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




