---
title: Interface INapClientManagement2 (NapManagement. h)
description: Fournit des méthodes pour la gestion des clients NAP. | Interface INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- NAP de l’interface INapClientManagement2
- INapClientManagement2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043056"
---
# <a name="inapclientmanagement2-interface"></a>Interface INapClientManagement2

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapClientManagement2** fournit des méthodes pour la gestion des clients NAP.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapClientManagement**](inapclientmanagement.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapClientManagement2** hérite de [**INapClientManagement**](inapclientmanagement.md). **INapClientManagement2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapClientManagement2** possède ces méthodes.



| Méthode                                                                                                    | Description                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Récupère les informations relatives à l’état d’isolement et à l’état d’isolement étendu du client NAP.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





