---
title: Valeurs de Registre pour la sécurité System-Wide
description: Valeurs de Registre pour la sécurité System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998878"
---
# <a name="registry-values-for-system-wide-security"></a>Valeurs de Registre pour la sécurité System-Wide

Il n’est pas recommandé de modifier les paramètres de sécurité à l’ensemble du système, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez les paramètres de sécurité à l’ensemble du système pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité Process-Wide](setting-processwide-security.md).

Certaines valeurs du Registre sont utilisées pour déterminer les paramètres de sécurité des applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Vous pouvez utiliser Dcomcnfg.exe pour modifier ces paramètres de sécurité par défaut pour un ordinateur. Pour obtenir des procédures pas à pas qui décrivent comment utiliser Dcomcnfg.exe à cet effet, consultez [définition de la sécurité des System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Une autre façon de modifier les paramètres par défaut à l’ensemble du système consiste à manipuler les valeurs de Registre directement. Toutefois, seuls les administrateurs et le système ont un accès complet à la partie du Registre qui contient les paramètres de sécurité par défaut des appels à l’échelle du système. Tous les autres utilisateurs disposent uniquement d’un accès en lecture.

Les valeurs nommées qui affectent les paramètres de sécurité par défaut à l’ensemble du système sont les suivantes :

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




