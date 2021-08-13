---
title: Comptes de service et BITS
description: Vous pouvez utiliser BITS pour transférer des fichiers à partir d’un service. Le service doit utiliser le compte système LocalSystem, LocalService ou NetworkService. Ces comptes sont toujours connectés ; par conséquent, les travaux soumis par un service à l’aide de ces comptes s’exécutent toujours.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- BITS de comptes de service
- transférer les BITS du travail, la propriété, le compte de service
- BITS de proxy, comptes de service
- informations d’identification pour transférer les BITS de travail
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679901"
---
# <a name="service-accounts-and-bits"></a>Comptes de service et BITS

Vous pouvez utiliser BITS pour transférer des fichiers à partir d’un service. Le service doit utiliser le compte système LocalSystem, LocalService ou NetworkService. Ces comptes sont toujours connectés ; par conséquent, les travaux soumis par un service à l’aide de ces comptes s’exécutent toujours.

Si un service s’exécutant sous un compte système emprunte l’identité de l’utilisateur avant d’appeler BITS, le service BITS répond comme pour n’importe quel compte d’utilisateur (par exemple, l’utilisateur doit être connecté à l’ordinateur pour que le transfert se produise). Le service doit également utiliser le masquage dynamique avec les pointeurs d’interface BITS lors de l’emprunt de l’identité de l’utilisateur. Le masquage n’étant pas hérité, vous devez appeler la fonction [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur chaque pointeur d’interface que vous recevez de bits (par exemple, le pointeur de travail retourné par l’appel de la méthode [**IBackgroundCopyManager :: createJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) ); Il n’est pas suffisant de définir le masquage sur le pointeur d’interface du gestionnaire. Vous pouvez également appeler la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour le processus au lieu d’appeler la fonction **CoSetProxyBlanket** sur chaque pointeur d’interface.

Toutefois, si le service n’emprunte pas l’identité de l’utilisateur, les comportements suivants s’appliquent :

- Les travaux créés par le compte de service sont détenus par ce compte. Étant donné que les comptes système sont toujours connectés, BITS transfère les fichiers tant que l’ordinateur est en cours d’exécution et qu’il existe une connexion réseau.
- Les comptes système ne doivent pas utiliser de lettres de lecteurs réseau mappés, car les lettres de lecteur sont spécifiques à une session et le mappage peut être perdu après le redémarrage de l’ordinateur.
- En l’absence d’un [jeton d’assistance](helper-tokens-for-bits-transfer-jobs.md), l’authentification réseau utilise les informations d’identification de l’ordinateur pour les comptes LocalSystem et NetworkService et les informations d’identification anonymes pour le compte LocalService. BITS retourne « accès refusé » si la liste de contrôle d’accès (ACL) pour le fichier source limite l’accès à un compte d’utilisateur.
- Pour plus d’informations sur le fonctionnement de l’authentification en présence d’un [jeton d’assistance](helper-tokens-for-bits-transfer-jobs.md), consultez [authentification](authentication.md).
- Les paramètres de proxy de Microsoft Internet Explorer sont stockés par utilisateur et ne sont pas définis pour les comptes système. Envisagez de configurer un jeton d’assistance sur vos travaux BITS ou de définir explicitement les paramètres de proxy appropriés en appelant [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) with **BG \_ Job \_ proxy \_ usage \_ override**. Vous pouvez également utiliser les commutateurs **/util/SetIEProxy** de BitsAdmin.exe pour définir les paramètres de proxy d’Internet Explorer pour le compte système LocalSystem, LocalService ou NetworkService. Pour plus d’informations, consultez [BitsAdmin Tool](bitsadmin-tool.md).

Notez que le service BITS ne reconnaît pas les paramètres de proxy qui sont définis à l’aide du fichier Proxycfg.exe.