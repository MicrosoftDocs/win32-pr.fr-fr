---
title: LegacyAuthenticationLevel
description: Définit le niveau d’authentification par défaut pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valeur de Registre LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029860"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Définit le niveau d’authentification par défaut pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **\_ mot reg** qui est équivalente aux \_ \_ constantes de niveau d’authentification RPC C \_ .



| Valeur | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ Authn \_ niveau \_ aucun           |
| 2     | \_ \_ \_ connexion au niveau AUTHn C RPC \_        |
| 3     | \_ \_ \_ appel au niveau d’authentification RPC C \_           |
| 4     | protocole d’authentification de l' \_ authentification RPC C \_ \_ \_            |
| 5     | \_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_ |
| 6     | \_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_   |



 

Si cette valeur de Registre est absente, le niveau d’authentification par défaut établi par le système est 2 (RPC \_ C \_ Authn \_ Connect).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




