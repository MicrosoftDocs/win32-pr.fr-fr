---
description: Représente un périphérique clavier synthétique.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543653"
---
# <a name="msvm_synthetickeyboard-class"></a>MSVM \_ SyntheticKeyboard, classe

Représente un périphérique clavier synthétique.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SyntheticKeyboard** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ SyntheticKeyboard** possède ces méthodes.



| Méthode                                                                  | Description                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | Demande un changement d’État.<br/> |
| [**Réinitialiser**](msvm-synthetickeyboard-reset.md)                           | réinitialise l’appareil.<br/>       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_USERDEVICE CIM**](cim-userdevice.md)
</dt> </dl>

 

 




