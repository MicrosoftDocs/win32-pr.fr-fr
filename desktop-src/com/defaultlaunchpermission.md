---
title: DefaultLaunchPermission
description: Définit la liste de Access Control (ACL) des principaux qui peuvent lancer des classes qui ne spécifient pas leur propre ACL via la valeur de Registre LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valeur de Registre DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b1ad6515186015055a353aa0dc87992cea9fccfbde46332e1a5d96c0a889f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993299"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Définit la liste de Access Control (ACL) des principaux qui peuvent lancer des classes qui ne spécifient pas leur propre ACL via la valeur de Registre [**LaunchPermission**](launchpermission.md) .

> [!Caution]  
> Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** .

Les autorisations d’accès par défaut sont les suivantes :

-   Administrateurs : autoriser le lancement
-   SYSTÈME : autoriser le lancement
-   INTERACTIF : autoriser le lancement

Si la valeur [**LaunchPermission**](launchpermission.md) est définie pour un serveur, elle est prioritaire sur la valeur **DefaultLaunchPermission** . Lors de la réception d’une demande locale ou distante pour lancer un serveur dont la clé [**AppID**](appid-key.md) n’a pas sa propre valeur **LaunchPermission** , la liste de contrôle d’accès décrite par cette valeur est vérifiée en usurpant l’identité du client et sa réussite autorise ou interdit le lancement du code de la classe.

Cette valeur fournit un niveau simple d’administration centralisée de l’accès par défaut au lancement des classes non gérées sur un ordinateur. Par exemple, un administrateur peut utiliser l’outil DCOMCNFG pour configurer le système afin d’autoriser l’accès en lecture seule pour les utilisateurs avec pouvoir. OLE limite donc les demandes de lancement du code de la classe aux membres du groupe utilisateurs avec pouvoir. Un administrateur peut ensuite configurer des autorisations de lancement pour des classes individuelles afin d’accorder la possibilité de lancer le code de classe à d’autres groupes ou utilisateurs individuels en fonction des besoins.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




