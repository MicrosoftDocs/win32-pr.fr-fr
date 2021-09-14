---
title: Définition de la sécurité Process-Wide dans le registre
description: Si vous souhaitez définir la sécurité pour un processus entier, une solution consiste à définir les niveaux de sécurité souhaités dans le registre.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311042"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Définition de la sécurité Process-Wide dans le registre

Si vous souhaitez définir la sécurité pour un processus entier, une solution consiste à définir les niveaux de sécurité souhaités dans le registre. Si votre application ne peut pas appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou si vous préférez ne pas utiliser la sécurité par programmation, cela peut être une bonne option. Si vous décidez de définir la sécurité au niveau du processus à l’aide du Registre, sachez que si vous appelez **CoInitializeSecurity** au sein de votre programme, vous utiliserez les valeurs dans **CoInitializeSecurity** et ignorez les valeurs de registre.

Il existe deux façons de définir la sécurité dans le registre de votre application :

-   Vous pouvez utiliser Dcomcnfg.exe, qui fournit une interface utilisateur simple pour modifier les valeurs de sécurité. Tous les serveurs COM peuvent être configurés à l’aide de Dcomcnfg.exe. Pour plus d’informations, consultez Définition de la [sécurité Process-Wide à l’aide de DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Toutefois, les applications clientes n’apparaissent normalement pas dans Dcomcnfg.exe, sauf si le client crée un GUID et l’entre dans le registre.
-   Vous pouvez définir des valeurs de sécurité sous la clé [AppID](appid-key.md) pour l’application. Le reste de cette rubrique explique comment définir la sécurité dans le registre à l’aide de la clé **AppID** .

Un AppID est un GUID qui représente un processus serveur pour une ou plusieurs classes. Chaque classe est associée à un seul AppID, et les AppID ne peuvent être affectés qu’à des exe. Les dll n’obtiennent pas d’AppID à moins qu’elles ne s’exécutent dans un substitut, puis il s’agit du processus de substitution qui a l’AppID. Si plusieurs dll sont chargées dans un substitut, chaque substitut n’a qu’un seul AppID.

Pour certains serveurs COM, le code d’inscription génère une AppID et place dans le registre les entrées qui mappent l’AppID au nom de l’exécutable. Toutefois, certains serveurs COM n’offrent pas cette fonctionnalité. Toutefois, si le code d’inscription du serveur ajoute une entrée pour HKCR \\ CLSID {ServerCLSID} \\ [LocalServer32](localserver32.md) lors de l’exécution de dcomcnfg.exe, il ajoute automatiquement un AppID pour le CLSID.

Pour un client COM qui n’est pas un serveur, ce mappage n’est pas créé, car le client n’est jamais inscrit. Par conséquent, pour définir la sécurité à l’aide de la clé **AppID** , le client doit créer les entrées de Registre nécessaires, soit par programme à l’aide des [fonctions de registre](/windows/desktop/SysInfo/registry-functions) , soit à l’aide de Regedit.

Si vous décidez de définir la sécurité au niveau du processus dans le Registre sous la clé **AppID** , sachez qu’il existe deux valeurs nommées sous la clé **AppID** que vous pouvez définir sans disposer des autorisations d’administrateur :

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Les valeurs **AuthenticationLevel** et **AccessPermission** sont définies indépendamment et ont des valeurs par défaut distinctes. Si la valeur **AuthenticationLevel** n’est pas présente, la valeur [LegacyAuthenticationLevel](legacyauthenticationlevel.md) est utilisée comme valeur par défaut. De même, si la valeur **AccessPermission** n’est pas présente, la valeur [DefaultAccessPermission](defaultaccesspermission.md) est utilisée comme valeur par défaut. Toutefois, les valeurs **AuthenticationLevel** et **AccessPermission** sont interdépendantes des manières suivantes :

-   Si **AuthenticationLevel** a la valeur None, les valeurs **AccessPermission** et **DefaultAccessPermission** sont ignorées pour cette application.
-   Si **AuthenticationLevel** n’est pas présent et que **LegacyAuthenticationLevel** a la valeur None, les valeurs **AccessPermission** et **DefaultAccessPermission** sont ignorées pour cette application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 