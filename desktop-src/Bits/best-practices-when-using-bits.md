---
title: Meilleures pratiques lors de l’utilisation de BITS
description: Cette section contient des informations que vous devez prendre en compte lors de la conception d’une application qui utilise BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939733"
---
# <a name="best-practices-when-using-bits"></a>Meilleures pratiques lors de l’utilisation de BITS

Cette section contient des informations que vous devez prendre en compte lors de la conception d’une application qui utilise BITS.

## <a name="user-context-or-service-context"></a>Contexte utilisateur ou contexte de service

BITS transfère les fichiers uniquement lorsque le propriétaire du travail est connecté à l’ordinateur (l’utilisateur doit avoir ouvert une session de manière interactive). BITS ne prend pas en charge la commande **runas** . Pour plus d’informations, consultez [utilisateurs et connexions réseau](users-and-network-connections.md).

Si vous n’avez pas besoin du contexte d’un utilisateur pour votre application, envisagez d’écrire un service qui s’exécute en tant que LocalSystem, LocalService ou NetworkService à la place. Ces comptes système étant toujours connectés, le transfert n’est pas soumis à un utilisateur qui se déconnecte. Toutefois, si vous empruntez l’identité d’un utilisateur lors de la création du travail, les règles de connexion interactives s’appliquent. Pour plus d’informations, consultez [comptes de service et bits](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>Les travaux sont persistants

Les travaux restent dans la file d’attente jusqu’à ce que vous appeliez la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . Les fichiers du travail ne sont pas accessibles à l’utilisateur tant que vous n’avez pas **terminé**. En règle générale, vous appelez **Complete** lorsque l’état du travail est **État du \_ travail BG \_ \_ transféré** et que vous appelez **Annuler** lorsque le travail est dans l’état d’erreur temporaire de l' **\_ État du travail \_ \_ \_ BG** ou de l' **\_ État du travail \_ \_ BG** et qu’il ne peut plus progresser.

Si vous n’appelez pas la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou la méthode [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dans un délai de 90 jours (valeur par défaut [paramètre jobinactivitytimeout](group-policies.md) stratégie de groupe), le service annule le travail. Vous devez toujours appeler la méthode **Complete** ou **Cancel** et ne pas compter sur la stratégie paramètre jobinactivitytimeout pour nettoyer vos travaux. Les travaux laissés dans la file d’attente peuvent empêcher les utilisateurs de créer d’autres travaux si la limite de stratégie MaxJobsPerUser ou MaxJobsPerMachine est atteinte.

## <a name="when-to-use-foreground-or-background-priority"></a>Quand utiliser la priorité de premier plan ou d’arrière-plan

À moins que le travail soit critique dans le temps ou que l’utilisateur attende activement, vous devez toujours utiliser une priorité d’arrière-plan. Toutefois, il peut arriver que vous souhaitiez passer de la priorité d’arrière-plan à la priorité de premier plan, par exemple lorsque le proxy ou le serveur ne prend pas en charge l’en-tête Content-Range, ou que le logiciel antivirus sur le client supprime la demande d’en-tête Range. Le passage à la priorité de premier plan fonctionne uniquement pour les fichiers dont la taille de fichier est inférieure à 2 Go. Pour obtenir un exemple, consultez l’implémentation de la méthode [**IBackgroundCopyCallback :: JobError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . Notez également que si la tâche de premier plan est ensuite interrompue en raison d’une déconnexion du réseau ou de la fermeture de session de l’utilisateur, le travail échouera car le service BITS enverra une demande de plage pour tenter de redémarrer le transfert à partir de là où il s’était arrêté.

À compter de Windows 8, vous devez configurer les travaux de téléchargement avec le **\_ \_ \_ \_ contenu dynamique de propriété de travail bits** et le premier niveau de **\_ \_ priorité \_ du travail BG** lorsque vous ciblez des serveurs qui ne répondent pas aux [exigences http pour les téléchargements bits](http-requirements-for-bits-downloads.md). Gardez à l’esprit que cela entraînera le redémarrage du téléchargement par BITS s’il est interrompu (par exemple, en raison de problèmes de connectivité ou de redémarrage du système).

Pour plus d’informations sur les priorités disponibles et la façon dont le service BITS utilise le niveau de priorité pour planifier des travaux, consultez la page [**\_ \_ priorité du travail BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Erreurs temporaires et irrécupérables

Certaines erreurs sont récupérables et d’autres non. Par exemple, l’erreur « le serveur n’est pas disponible » est une erreur récupérable et l’erreur « Accès refusé » est une erreur irrécupérable. BITS place les erreurs récupérables dans un état d’erreur temporaire et tente à nouveau la tâche après un intervalle spécifié. Si le travail ne parvient pas à progresser, le service BITS déplace la tâche vers un état d’erreur irrécupérable. Utilisez les méthodes [**méthode ibackgroundcopyjob :: SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) et [**méthode ibackgroundcopyjob :: SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) pour contrôler la façon dont bits traite les erreurs temporaires.

Pour les tâches de premier plan, vous devez limiter la durée pendant laquelle vous laissez un travail dans l’état d’erreur temporaire et essayez de récupérer. Utilisez la méthode [**SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) pour limiter la durée pendant laquelle un travail reste dans un état d’erreur temporaire ou pour forcer le travail dans l’état d’erreur irrécupérable. Si vous laissez la tâche essayer de récupérer, vous devez utiliser la méthode [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) pour définir le délai minimal entre deux tentatives sur 60 secondes ou appeler la méthode [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour réactiver la tâche.

Pour plus d’informations, [**consultez \_ \_ État de la tâche BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [cycle de vie d’une tâche bits](life-cycle-of-a-bits-job.md)et [gestion des erreurs](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Mesure de l’utilisation de la bande passante réseau

BITS peut utiliser la carte réseau du client pour estimer la bande passante réseau disponible. Étant donné que le service BITS n’est pas en mesure de mesurer la bande passante au-delà du client, BITS peut encombrer la liaison WAN. Pour réduire l’encombrement sur la liaison de réseau étendu (WAN), vous pouvez utiliser la stratégie de groupe **MaxInternetBandwidth** pour limiter la quantité de bande passante utilisée par le client. Pour plus d’informations, consultez [bande passante réseau](network-bandwidth.md) et [stratégies de groupe](group-policies.md).

Si vous écrivez une application que de nombreux clients utiliseront pour télécharger des fichiers à partir d’un serveur donné, vous devez envisager un modèle qui étale les demandes de téléchargement afin de ne pas surcharger le serveur avec les demandes.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Définition des informations d’identification pour l’authentification du proxy et du serveur

Si vous vous attendez à ce que le proxy ou le serveur requière des informations d’identification de l’utilisateur, vous devez fournir les informations d’identification au service BITS. Pour spécifier les informations d’identification, appelez la méthode [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . BITS prend en charge les schémas d’authentification de base, Digest, Negotiate, NTLM et Passport.

Pour plus d’informations sur l’authentification, consultez [authentification](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Spécification des paramètres de proxy pour les comptes d’utilisateur et les comptes de service

Par défaut, le service BITS utilise les paramètres de proxy d’Internet Explorer de l’utilisateur. Pour remplacer les paramètres de proxy d’Internet Explorer de l’utilisateur, appelez la méthode [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) .

Les paramètres de proxy d’Internet Explorer ne s’appliquent pas aux comptes système. par conséquent, le comportement du proxy par défaut (**\_ \_ \_ \_ préconfiguration de l’utilisation du proxy de la tâche BG**) fonctionne uniquement dans les déploiements du protocole WPAD (Web Proxy Auto-Discovery), sauf si des étapes de configuration supplémentaires sont effectuées. Si votre application est un service qui s’exécute en tant que LocalSystem, LocalService ou NetworkService, envisagez de configurer un jeton d’assistance sur vos travaux BITS ou de définir explicitement les paramètres de proxy appropriés en appelant [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) avec le **\_ \_ \_ \_ remplacement de l’utilisation du proxy de tâche BG**. Vous pouvez également utiliser les commutateurs **/util/SetIEProxy** de BitsAdmin.exe pour définir les paramètres de proxy d’Internet Explorer pour le compte système LocalSystem, LocalService ou NetworkService. Pour plus d’informations, consultez [BitsAdmin Tool](bitsadmin-tool.md).

Le service BITS ne reconnaît pas les paramètres de proxy qui sont définis à l’aide du fichier Proxycfg.exe.

À compter de la mise à jour 2018 de Windows 10 octobre (10,0 ; Build 17763), BITS utilise la même commande de proxy que celle utilisée par WinHttp avec AUTOMATIC_PROXY. BITS utilise ce classement plus compatible lorsque BG_JOB_PROXY_USAGE_PRECONFIG est spécifié. BG_JOB_PROXY_USAGE_PRECONFIG est la valeur par défaut pour la spécification du proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Spécification de paramètres spécifiques à l’utilisateur pour l’authentification des proxies

Si vous utilisez BITS dans un environnement qui requiert l’authentification du proxy lors de l’exécution en tant que compte sans informations d’identification NTLM ou Kerberos utilisables dans le domaine réseau de l’ordinateur, vous devez effectuer des étapes supplémentaires pour vous authentifier correctement à l’aide des informations d’identification d’un autre compte d’utilisateur qui possède des informations d’identification sur le domaine. Il s’agit d’un scénario classique dans lequel votre code BITS s’exécute en tant que service système tel que LocalService, NetworkService ou LocalSystem, car ces comptes n’ont pas d’informations d’identification NTLM ou Kerberos utilisables.

Pour plus d’informations sur le fonctionnement de l’authentification dans ce scénario, consultez [authentification.](authentication.md)

## <a name="scalability"></a>Extensibilité

Si plus de 100 travaux se trouvent dans la file d’attente, les performances peuvent commencer à diminuer en fonction de la composition du travail. BITS utilise le paramètre de stratégie [MaxJobsPerMachine](group-policies.md) pour imposer une limite inconditionnelle du nombre de travaux dans la file d’attente. Les applications doivent limiter le nombre de leurs travaux à environ 10, de sorte que plusieurs applications auront moins de chance de dépasser les indications 100-Job. En règle générale, une application avec un grand nombre de tâches à soumettre commence par envoyer 10 tâches, puis envoie l’une après l’autre, à la fin de chaque travail.

Le nombre de fichiers dans le travail doit également être limité à un maximum de 10 fichiers. Si vous souhaitez transférer un grand nombre de fichiers pour un travail, envisagez de créer un fichier CAB qui contient tous les fichiers à la place.

## <a name="http-headers-can-be-in-any-case"></a>Les en-têtes HTTP peuvent être dans tous les cas

Les normes HTTP ont toujours dit que les en-têtes HTTP doivent être traités comme ne respectant pas la casse (RFC 7230 section 3,2). La norme HTTP la plus récente, RFC 7540, va plus loin et indique que le trafic HTTP/2 doit comparer les en-têtes comme non sensibles à la casse et doit présenter des en-têtes en minuscules (RFC 6540, section 8.1.2). Même lorsque le trafic est envoyé avec des en-têtes qui ne sont pas en minuscules, les proxies peuvent choisir de forcer les en-têtes en minuscules.

## <a name="avoiding-personally-identifiable-information-pii"></a>Éviter les informations d’identification personnelle (PII)

Les tâches BITS, y compris le nom d’affichage et la description et les noms de fichiers, sont visibles par tous les utilisateurs disposant de privilèges d’administrateur. Ils peuvent également être ajoutés à la télémétrie Windows. Vous devez éviter de placer des données sensibles (telles que le nom de l’utilisateur) dans les détails du travail.
