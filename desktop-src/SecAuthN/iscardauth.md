---
description: La définition de l’interface ISCardAuth est fournie en tant que norme qui peut être suivie lors du développement d’un fournisseur de services de carte à puce. L’interface ISCardAuth peut être utilisée pour exposer des services d’authentification pris en charge par une carte à puce.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interface ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484721"
---
# <a name="iscardauth-interface"></a>Interface ISCardAuth

\[L’interface **ISCardAuth** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La définition de l’interface **ISCardAuth** est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .

L’interface **ISCardAuth** peut être utilisée pour exposer des services d’authentification pris en charge par une carte à puce. Ces services incluent l’authentification de l’application, l’authentification par carte à puce et l’authentification des utilisateurs.

L’exemple suivant illustre une utilisation type de l’interface **ISCardAuth** .

**Pour utiliser ISCardAuth**

1.  Créez une interface **ISCardAuth** (à l’aide de la méthode d’interface [**ISCardManage**](iscardmanage.md) correspondante).
2.  Appelez la méthode **ISCardAuth** appropriée ([**\_ authentification**](iscardauth-app-auth.md)de l’application, [**GetChallenge**](iscardauth-getchallenge.md), [**\_ authentification ICC**](iscardauth-icc-auth.md)ou [**\_ authentification utilisateur**](iscardauth-user-auth.md)).
3.  Libérez l’interface **ISCardAuth** .

## <a name="members"></a>Membres

L’interface **ISCardAuth** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardAuth** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardAuth** possède ces méthodes.



| Méthode                                          | Description                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Authentification de l’application \_**](iscardauth-app-auth.md)        | Permet à l’application de s’authentifier à l’aide d’un protocole de stimulation/signature.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Retourne une stimulation de la carte à puce.<br/>                                            |
| [**\_Authentification ICC**](iscardauth-icc-auth.md)        | Permet à une application d’authentifier la carte à puce.<br/>                               |
| [**\_Authentification utilisateur**](iscardauth-user-auth.md)      | Autorise l’accès aux services d’authentification des utilisateurs.<br/>                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 

 
