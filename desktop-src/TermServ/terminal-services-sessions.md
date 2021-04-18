---
title: Sessions Bureau à distance
description: Étant donné que chaque connexion à un client Connexion Bureau à distance (RDC) reçoit un ID de session distinct, l’expérience utilisateur est semblable à la connexion à plusieurs ordinateurs en même temps. par exemple, un ordinateur de bureau et un ordinateur privé.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511896"
---
# <a name="remote-desktop-sessions"></a>Sessions Bureau à distance

Lorsqu’un utilisateur se connecte à un ordinateur Services Bureau à distance, une session est démarrée pour l’utilisateur. Chaque session est identifiée par un ID de session unique. Étant donné que chaque connexion à un client Connexion Bureau à distance (RDC) reçoit un ID de session distinct, l’expérience utilisateur est semblable à la connexion à plusieurs ordinateurs en même temps. par exemple, un ordinateur de bureau et un ordinateur privé.

Chaque session Bureau à distance est associée à une station Windows Interactive. Le seul nom de station de fenêtre pris en charge pour une station Windows Interactive est « WinSta0 ». par conséquent, chaque session est associée à sa propre station de fenêtre « WinSta0 ». Il existe trois bureaux standard pour chaque station Windows : le bureau Winlogon, le Bureau de l’économiseur d’écran et le bureau interactif.

L’utilisateur associé à la station de fenêtre interactive pour une session est connu sous le nom d' *utilisateur interactif*. Sur un client Connexion Bureau à distance (RDC), il peut y avoir plusieurs utilisateurs interactifs en plus de l’utilisateur interactif sur la console Services Bureau à distance. Pour récupérer l’identificateur de la session actuellement attachée à la console, utilisez la fonction [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) .

Lorsqu’un utilisateur se déconnecte d’un client Connexion Bureau à distance (RDC), la session du client sur le serveur hôte de session Bureau à distance (anciennement appelé Terminal Server) est supprimée et les stations et postes de travail Windows associés à cette session sont supprimés. Toutefois, étant donné que la session de console Services Bureau à distance n’est jamais supprimée, les stations de fenêtres associées à la session de console ne sont pas supprimées. Cela affecte la façon dont les applications se comportent dans un environnement Services Bureau à distance lorsqu’elles sont configurées pour s’exécuter dans le contexte de sécurité de l’utilisateur interactif, également appelé mode d’activation d’objet « RunAs interactive User ».

Pour plus d’informations sur le démarrage d’un processus serveur local sur une session spécifiée, consultez Activation de session [à session à l’aide d’un moniker de session](session-to-session-activation-with-a-session-moniker.md) et utilisation d' [un moniker de session](using-a-session-moniker.md). Pour plus d’informations sur les contextes de sécurité, consultez [le contexte de sécurité du client](/windows/desktop/SecAuthZ/the-client-security-context).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sessions enfants](child-sessions.md)
</dt> </dl>

 

 