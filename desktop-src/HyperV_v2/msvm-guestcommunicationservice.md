---
description: Représente le service de communication invité. Il est utilisé pour la communication avec l’invité, à partir de l’hôte Hyper-V.
ms.assetid: 8d1d241f-4702-41bc-ab44-4f0aaa83ad4b
title: Classe Msvm_GuestCommunicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 900e943d6c728768b2f2d1d3f61740942f1da15bc8b1c09e28dcddde2dbe873c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523179"
---
# <a name="msvm_guestcommunicationservice-class"></a>MSVM \_ GuestCommunicationService, classe

Représente le service de communication invité. Il est utilisé pour la communication avec l’invité, à partir de l’hôte Hyper-V.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationService : Msvm_GuestService
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestCommunicationService** ne définit aucun membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




