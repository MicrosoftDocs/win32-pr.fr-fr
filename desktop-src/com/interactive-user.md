---
title: Utilisateur interactif
description: L’utilisateur interactif est l’utilisateur actuellement connecté à l’ordinateur sur lequel s’exécute le serveur COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363407"
---
# <a name="interactive-user"></a>Utilisateur interactif

L' *utilisateur interactif* est l’utilisateur actuellement connecté à l’ordinateur sur lequel s’exécute le serveur com. Si l’identité est définie comme étant l’utilisateur interactif, tous les clients utilisent la même instance du serveur si le serveur inscrit sa fabrique de classe en tant qu’utilisation multiple. Si aucun utilisateur n’est connecté, le serveur ne s’exécute pas. Si le serveur dispose d’une interface graphique utilisateur (GUI) que le client doit voir, vous devez utiliser l’utilisateur interactif pour l’identité du serveur. Toutefois, le choix de cette identité présente des risques de sécurité, car le serveur s’exécute sous l’identité de l’utilisateur connecté sans la connaissance ou le consentement de l’utilisateur connecté. En outre, une application de service ne peut pas afficher une interface utilisateur. Pour plus d’informations, consultez [services interactifs](/windows/desktop/Services/interactive-services).

Si un serveur COM est configuré pour s’exécuter en tant qu’utilisateur interactif, dans un environnement de services Terminal Server, le serveur est lancé dans la session interactive qui correspond à l’identité de l’utilisateur du client. Toutefois, l’application cliente peut utiliser le moniker de session pour référencer un objet fourni par le serveur dans une session qui ne correspond pas à l’identité du client. Lorsque cette fonction est utilisée, l’application cliente peut spécifier n’importe quelle session. dans ce cas, le serveur s’exécute en tant qu’utilisateur propriétaire de la session, et non à l’utilisateur exécutant. Les autorisations d’accès par défaut dans ce scénario ne permettent pas à l’utilisateur qui lance l’appel d’appeler des méthodes sur le serveur. Toutefois, les risques de sécurité suivants sont conservés :

-   Si le serveur COM expose des interfaces qui ne sont pas contrôlées par COM, telles que les ports TCP, les canaux nommés, les ports LPC, les sections de mémoire partagée, etc., elles peuvent être utilisées par l’utilisateur de lancement pour influencer le serveur. Les objets COM configurés pour s’exécuter en tant qu’utilisateur interactif doivent réduire autant que possible cette surface d’attaque.
-   Les objets COM sont libres de définir leurs propres autorisations d’accès. Si l’objet définit des autorisations d’accès, dans son inscription AppID ou en appelant [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), pour autoriser le lancement de l’accès utilisateur, l’utilisateur peut lancer le serveur pour qu’il s’exécute en tant qu’autre utilisateur, puis accéder à l’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Identité de l'application](application-identity.md)
</dt> <dt>

[Lancement de l’utilisateur](launching-user.md)
</dt> <dt>

[Identité du service](service-identity.md)
</dt> <dt>

[Utilisateur spécifié](specified-user.md)
</dt> </dl>

 

 