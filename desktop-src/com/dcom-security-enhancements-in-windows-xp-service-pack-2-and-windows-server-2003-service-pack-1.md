---
title: améliorations de la sécurité DCOM dans Windows XP service pack 2 et Windows Server 2003 service pack 1
description: Windows server XP service pack 2 (SP2) et Windows server 2003 service pack 1 (SP1) introduisent des paramètres de sécurité par défaut améliorés pour le modèle DCOM (Distributed Component Object Model).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d093186f3d0a028112248409b71e0d71ed084e15cc075a1aced7a589aa0733ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501329"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>améliorations de la sécurité DCOM dans Windows XP service pack 2 et Windows Server 2003 service pack 1

Windows server XP service pack 2 (SP2) et Windows server 2003 service pack 1 (SP1) introduisent des paramètres de sécurité par défaut améliorés pour le modèle DCOM (Distributed Component Object Model). Plus précisément, ils introduisent des droits plus granulaires qui permettent à un administrateur d’avoir un contrôle indépendant sur les autorisations locales et distantes pour le lancement, l’activation et l’accès aux serveurs COM.

## <a name="what-does-dcom-do"></a>Que fait DCOM ?

Le modèle COM (Component Object Model) Microsoft est un système orienté objet et indépendant de la plateforme, qui permet de créer des composants logiciels binaires pouvant interagir. Le modèle DCOM (Distributed Component Object Model) permet aux applications d’être distribuées dans différents emplacements, ce qui est le plus significatif pour vous et pour l’application. Le protocole DCOM prend en charge de manière transparente la prise en charge de communications fiables, sécurisées et efficaces entre les composants COM.

## <a name="who-does-this-feature-apply-to"></a>À qui cette fonctionnalité s'adresse-t-elle ?

Si vous utilisez COM uniquement pour les composants COM in-process, cette fonctionnalité ne s’applique pas à vous.

Cette fonctionnalité s’applique si vous disposez d’une application serveur COM qui répond à l’un des critères suivants :

-   L’autorisation d’accès pour l’application est moins stricte que l’autorisation d’exécution, ce qui est nécessaire pour exécuter l’application.
-   L’application est généralement activée par un client COM distant sans utiliser de compte administratif.
-   L’application est destinée à être utilisée uniquement localement. Cela signifie que vous pouvez restreindre votre application serveur COM afin qu’elle ne soit pas accessible à distance.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>quelles sont les nouvelles fonctionnalités ajoutées à cette fonctionnalité dans Windows XP service pack 2 et Windows Server 2003 service pack 1 ?

### <a name="computer-wide-restrictions"></a>Restrictions au niveau de l’ordinateur

Une modification a été apportée à COM pour fournir des contrôles d’accès à l’ensemble de l’ordinateur qui régissent l’accès à toutes les demandes d’appel, d’activation ou de lancement sur l’ordinateur. La façon la plus simple de réfléchir à ces contrôles d’accès est l’appel [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) supplémentaire effectué sur une liste de contrôle d’accès à l’ensemble de l’ordinateur (ACL) à chaque appel, activation ou lancement d’un serveur com sur l’ordinateur. Si **AccessCheck** échoue, la demande d’appel, d’activation ou de lancement est refusée. Cela s’ajoute à tous les **AccessCheck** qui sont exécutés sur les listes de contrôle d’accès spécifiques au serveur. En effet, elle fournit une norme d’autorisation minimale qui doit être passée pour accéder à n’importe quel serveur COM sur l’ordinateur. Il existe une liste de contrôle d’accès (ACL) à l’ensemble de l’ordinateur pour les autorisations de lancement afin de couvrir les droits d’activation et de lancement, ainsi qu’une liste ACL à l’emplacement de l’ordinateur pour les autorisations d’accès aux Ils peuvent être configurés via la console MMC (Microsoft Management Console) des services de composants.

Ces listes de contrôle d’accès d’ordinateur offrent un moyen de remplacer les paramètres de sécurité faibles spécifiés par une application spécifique via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou les paramètres de sécurité spécifiques à l’application. Cela fournit une norme de sécurité minimale qui doit être transmise, quels que soient les paramètres du serveur spécifique.

Ces ACL sont vérifiées lors de l’accès aux interfaces exposées par RPCSS. Cela fournit une méthode pour contrôler l’accès à ce service système.

Ces listes de contrôle d’accès fournissent un emplacement centralisé dans lequel un administrateur peut définir une stratégie d’autorisation générale qui s’applique à tous les serveurs COM sur l’ordinateur.

> [!Note]  
> La modification des paramètres de sécurité au niveau de l’ordinateur affecte toutes les applications serveur COM et peut les empêcher de fonctionner correctement. Si des applications serveur COM présentent des restrictions moins strictes que les restrictions à l’niveau de l’ordinateur, la réduction des restrictions de l’ordinateur peut exposer ces applications à un accès indésirable. À l’inverse, si vous augmentez les restrictions au niveau de l’ordinateur, certaines applications serveur COM peuvent ne plus être accessibles en appelant des applications.

 

par défaut, les paramètres de restriction des ordinateurs Windows XP SP2 sont les suivants :



| Autorisation        | Administrateur                                                                                             | Tout le monde                                            | Anonyme               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Lancer<br/> | Lancement local<br/> Activation locale<br/> Lancement distant<br/> Activation distante<br/> | Lancement local<br/> Activation locale<br/> |                         |
| Accès<br/> |                                                                                                           | Accès local<br/> Accès à distance<br/>    | Accès local<br/> |



 

par défaut, les paramètres de restriction des ordinateurs Windows Server 2003 SP 1 sont les suivants.



| Autorisation        | Administrateur                                                                                             | Utilisateurs du modèle COM distribué (groupe intégré)                                                                    | Tout le monde                                            | Anonyme                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Lancer<br/> | Lancement local<br/> Activation locale<br/> Lancement distant<br/> Activation distante<br/> | Lancement local<br/> Activation locale<br/> Lancement distant<br/> Activation distante<br/> | Lancement local<br/> Activation locale<br/> | N/A<br/>                                   |
| Accès<br/> | N/A<br/>                                                                                            | Accès local<br/> Accès à distance<br/>                                                          | Accès local<br/> Accès à distance<br/>    | Accès local<br/> Accès à distance<br/> |



 

> [!Note]  
> les utilisateurs du modèle COM distribué sont un nouveau groupe intégré fourni avec Windows Server 2003 SP1 pour accélérer le processus d’ajout d’utilisateurs aux paramètres de restriction des ordinateurs DCOM. Ce groupe fait partie de la liste de contrôle d’accès utilisée par les paramètres [MachineAccessRestriction](machineaccessrestriction.md) et [MachineLaunchRestriction](machinelaunchrestriction.md) , de sorte que la suppression des utilisateurs de ce groupe affecte ces paramètres.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>En quoi cette modification est-elle importante ? Quelles menaces contribue-t-elle à limiter ?

De nombreuses applications COM incluent du code spécifique à la sécurité (par exemple, l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)), mais utilisent des paramètres faibles, ce qui permet souvent l’accès non authentifié au processus. Il n’existe actuellement aucun moyen pour un administrateur de remplacer ces paramètres pour forcer une sécurité renforcée dans les versions antérieures de Windows.

L’infrastructure COM comprend le RPCSS, un service système qui s’exécute pendant le démarrage du système et qui s’exécute toujours après cela. Il gère l’activation d’objets COM et la table d’objets en cours d’exécution et fournit des services d’assistance à la communication à distance DCOM. Il expose des interfaces RPC qui peuvent être appelées à distance. Étant donné que certains serveurs COM autorisent l’accès à distance non authentifié, ces interfaces peuvent être appelées par n’importe qui, y compris les utilisateurs non authentifiés. Par conséquent, le RPCSS peut être attaqué par des utilisateurs malveillants sur des ordinateurs distants non authentifiés.

dans les versions antérieures de Windows, un administrateur n’avait aucun moyen de comprendre le niveau d’exposition des serveurs COM sur un ordinateur. un administrateur a obtenu une idée du niveau d’exposition en vérifiant de manière systématique les paramètres de sécurité configurés pour toutes les applications COM inscrites sur l’ordinateur, mais étant donné qu’il y a environ 150 serveurs com dans une installation par défaut de Windows, cette tâche était décourageante. Il n’existait aucun moyen d’afficher les paramètres d’un serveur qui incorpore la sécurité dans le logiciel, à moins d’examiner le code source de ce logiciel.

Les restrictions DCOM à l’ensemble de l’ordinateur atténuent ces trois problèmes. Il permet également à un administrateur de désactiver l’activation, le lancement et les appels DCOM entrants.

### <a name="what-works-differently"></a>En quoi le fonctionnement est-il différent ?

Par défaut, le groupe tout le monde dispose des autorisations de lancement local, d’activation locale et d’appel d’accès local. Cela permet à tous les scénarios locaux de fonctionner sans modification du logiciel ou du système d’exploitation.

par défaut, dans Windows XP SP2, le groupe tout le monde est autorisé à accéder aux appels d’accès à distance. dans Windows Server 2003 SP1, les groupes tout le monde et anonymes disposent d’autorisations d’accès à distance. Cela permet la plupart des scénarios de client COM, y compris le cas courant où un client COM transmet une référence locale à un serveur distant, ce qui a pour effet de transformer le client en serveur. dans Windows XP SP2, cela peut désactiver les scénarios qui requièrent des appels d’accès à distance non authentifiés.

Par défaut, seuls les membres du groupe administrateurs bénéficient des autorisations d’activation à distance et de lancement. Cela désactive les activations à distance par des non-administrateurs sur les serveurs COM installés.

### <a name="how-do-i-resolve-these-issues"></a>Comment faire résoudre ces problèmes ?

Si vous implémentez un serveur COM et que vous prévoyez de prendre en charge l’activation à distance par un client COM non administratif, vous devez déterminer si le risque associé à l’activation de ce processus est acceptable ou si vous devez modifier votre implémentation pour ne pas exiger l’activation à distance par un client COM non administratif ou des appels non authentifiés distants.

Si le risque est acceptable et que vous souhaitez activer l’activation à distance par un client COM non administratif ou des appels non authentifiés distants, vous devez modifier la configuration par défaut de cette fonctionnalité.

> [!Note]  
> La modification des paramètres de sécurité au niveau de l’ordinateur affecte toutes les applications serveur COM et peut les empêcher de fonctionner correctement. Si des applications serveur COM présentent des restrictions moins strictes que les restrictions à l’niveau de l’ordinateur, la réduction des restrictions de l’ordinateur peut exposer ces applications à un accès indésirable. À l’inverse, si vous augmentez les restrictions au niveau de l’ordinateur, certaines applications serveur COM peuvent ne plus être accessibles en appelant des applications.

 

vous pouvez modifier les paramètres de configuration à l’aide des Services de composants Microsoft Management Console (MMC) ou du registre Windows.

Si vous utilisez le composant logiciel enfichable MMC services de composants, ces paramètres peuvent être configurés sous l’onglet **sécurité com** de la boîte de dialogue **Propriétés** de l’ordinateur que vous gérez. La zone **autorisations d’accès** a été modifiée pour vous permettre de définir des limites à l’ensemble de l’ordinateur en plus des paramètres par défaut standard des serveurs com. En outre, vous pouvez fournir des paramètres ACL distincts pour l’accès local et à distance dans les limites et les valeurs par défaut.

Dans la zone **autorisations d’exécution et d’activation** , vous pouvez contrôler les autorisations locales et distantes, ainsi que les limites à l’ensemble de l’ordinateur et les valeurs par défaut. Vous pouvez spécifier à la fois l’activation locale et à distance et lancer des autorisations indépendamment.

Vous pouvez également configurer ces paramètres de liste de contrôle d’accès à l’aide du Registre.

Ces listes de contrôle d’accès sont stockées dans le registre aux emplacements suivants :

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Il s’agit de valeurs nommées de type REG \_ Binary qui contiennent des données qui décrivent l’ACL des principaux qui peuvent accéder à n’importe quelle classe com ou objet com sur l’ordinateur. Les droits d’accès dans la liste de contrôle d’accès sont les suivants :

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Ces listes de contrôle d’accès peuvent être créées à l’aide de fonctions de sécurité normales.

> [!Note]  
> pour assurer la compatibilité descendante, une liste de contrôle d’accès peut exister au format utilisé avant Windows XP SP2 et Windows Server 2003 SP1, qui utilise uniquement les droits com access right \_ \_ s’exécutent, ou il peut exister dans le nouveau format utilisé dans Windows XP SP2 et Windows Server 2003 SP1, qui utilise des \_ droits com \_ s’exécutent avec une combinaison de droits com execute \_ local, les droits \_ \_ com \_ \_ execute \_ remote, les \_ droits com \_ activate \_ local et les \_ droits com \_ activate \_ remote. Notez que \_ les droits com \_ s’exécutent> doivent toujours être présents ; l’absence de ce droit génère un descripteur de sécurité non valide. Notez également que vous ne devez pas mélanger l’ancien format et le nouveau format dans une ACL unique. toutes les entrées de contrôle d’accès (ACE, Access Control Entry) doivent accorder uniquement le \_ \_ droit d’accès d’exécution des droits com, ou elles doivent toutes accorder des \_ droits com \_ en association avec une combinaison de \_ droits com \_ Execute \_ local, les \_ droits com \_ Execute \_ Remote, les \_ droits com \_ active \_ locale et les \_ droits com \_ Activate \_ Remote.

 

> [!Note]  
> Seuls les utilisateurs disposant de droits d’administrateur peuvent modifier ces paramètres.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>quelles fonctionnalités existantes évoluent dans Windows XP service pack 2 et Windows Server 2003 service pack 1 ?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS s’exécute en tant que service réseau

RPCSS est un service de clés pour le mappeur de point de terminaison RPC et l’infrastructure DCOM. Ce service a été exécuté en tant que système local dans les versions précédentes de Windows. pour réduire la surface d’attaque de Windows et fournir une défense en profondeur, la fonctionnalité du service RPCSS a été divisée en deux services. Le service RPCSS avec toutes les fonctionnalités d’origine qui ne nécessitaient pas de privilèges système local s’exécute désormais sous le compte service réseau. Un nouveau service DCOMLaunch qui comprend des fonctionnalités nécessitant des privilèges du système local s’exécute sous le compte système local.

### <a name="why-is-this-change-important"></a>En quoi cette modification est-elle importante ?

Cette modification réduit la surface d’attaque et fournit une défense en profondeur pour le service RPCSS, car une élévation de privilèges dans le service RPCSS est désormais limitée au privilège de service réseau.

### <a name="what-works-differently"></a>En quoi le fonctionnement est-il différent ?

Cette modification doit être transparente pour les utilisateurs, car la combinaison des services RPCSS et DCOMLaunch est équivalente au service RPCSS précédent fourni dans les versions antérieures de Windows.

### <a name="more-specific-com-permissions"></a>Autorisations COM plus spécifiques

Les applications serveur COM ont deux types d’autorisations : les autorisations de lancement et les autorisations d’accès. Les autorisations de lancement contrôlent l’autorisation de démarrer un serveur COM lors de l’activation COM si le serveur n’est pas déjà en cours d’exécution. Ces autorisations sont définies en tant que descripteurs de sécurité spécifiés dans les paramètres du Registre. Les autorisations d’accès contrôlent l’autorisation d’appeler un serveur COM en cours d’exécution. Ces autorisations sont définies en tant que descripteurs de sécurité fournis à l’infrastructure COM par le biais de l’API [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , ou à l’aide des paramètres du Registre. Les autorisations d’exécution et d’accès autorisent ou refusent l’accès en fonction des principaux, et n’effectuent aucune distinction quant à la nécessité ou non de faire en sorte que l’appelant soit local au serveur ou distant.

La première modification distingue les droits d’accès COM en fonction de la distance. Les deux distances définies sont local et distant. Un message COM local est reçu par le biais du protocole d’appel de procédure distante locale (LRPC), tandis qu’un message COM distant arrive au moyen d’un protocole hôte d’appel de procédure distante (RPC) comme le protocole TCP (Transmission Control Protocol).

L’activation COM consiste à obtenir un proxy d’interface COM sur un client en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou l’une de ses variantes. En tant qu’effet secondaire de ce processus d’activation, un serveur COM doit parfois être démarré pour satisfaire la demande du client. Une liste de contrôle d’accès des autorisations de lancement indique qui est autorisé à démarrer un serveur COM. Une liste de contrôle d’accès des autorisations d’accès déclare qui est autorisé à activer un objet COM ou à appeler cet objet une fois que le serveur COM est déjà en cours d’exécution.

La deuxième modification est que les droits d’appel et d’activation sont séparés pour refléter deux opérations distinctes et pour déplacer le droit d’activation de l’ACL d’autorisation d’accès vers l’ACL d’autorisation Launch. Étant donné que l’activation et le lancement sont tous deux liés à l’acquisition d’un pointeur d’interface, l’activation et le lancement de droits d’accès appartiennent logiquement à une liste de contrôle d’accès. Et étant donné que vous spécifiez toujours des autorisations de lancement via la configuration (par rapport aux autorisations d’accès, qui sont souvent spécifiées par programmation), le fait de placer les droits d’activation dans la liste de contrôle d’accès de lancement permet à l’administrateur de contrôler l’activation.

Les entrées de contrôle d’accès (ACE) de lancement sont divisées en quatre droits d’accès :

-   Lancement local (LL)
-   Lancement à distance (RL)
-   Activation locale (LA)
-   Activation à distance (RA)

Le descripteur de sécurité d’autorisation d’accès est divisé en deux droits d’accès :

-   Appels d’accès local (LC)
-   Appels d’accès à distance (RC)

Cela permet à l’administrateur d’appliquer des configurations de sécurité très spécifiques. Par exemple, vous pouvez configurer un serveur COM afin qu’il accepte les appels d’accès locaux de tout le monde, tout en acceptant uniquement les appels d’accès à distance des administrateurs. Ces distinctions peuvent être spécifiées par le biais de modifications apportées aux descripteurs de sécurité des autorisations COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>En quoi cette modification est-elle importante ? Quelles menaces contribue-t-elle à limiter ?

Les versions antérieures de l’application serveur COM n’ont aucun moyen de limiter une application afin qu’elle puisse être utilisée uniquement localement sans exposer l’application sur le réseau par le biais de DCOM. Lorsqu’un utilisateur a accès à une application serveur COM, il a accès à la fois à l’utilisation locale et à distance.

Une application serveur COM peut s’exposer à des utilisateurs non authentifiés pour implémenter un scénario de rappel COM. Dans ce scénario, l’application doit également exposer son activation à des utilisateurs non authentifiés, ce qui peut ne pas être souhaitable.

Les autorisations COM précises confèrent à l’administrateur la possibilité de contrôler la stratégie d’autorisation COM d’un ordinateur. Ces autorisations activent la sécurité pour les scénarios décrits.

### <a name="what-works-differently-are-there-any-dependencies"></a>En quoi le fonctionnement est-il différent ? Existe-t-il des dépendances ?

Pour assurer la compatibilité descendante, les descripteurs de sécurité COM existants sont interprétés pour autoriser ou refuser l’accès local et distant simultanément. Autrement dit, une entrée de contrôle d’accès (ACE, Access Control Entry) autorise à la fois local et distant, ou refuse à la fois local et distant.

Il n’existe aucun problème de compatibilité descendante pour les droits d’appel ou de lancement. Toutefois, il existe un problème de compatibilité des droits d’activation. Si, dans les descripteurs de sécurité existants pour un serveur COM, les autorisations de lancement configurées sont plus restrictives que les autorisations d’accès et sont plus restrictives que ce qui est requis au minimum pour les scénarios d’activation du client, l’ACL des autorisations d’exécution doit être modifiée pour permettre aux clients autorisés d’accéder aux autorisations d’activation appropriées.

Pour les applications COM qui utilisent les paramètres de sécurité par défaut, il n’existe aucun problème de compatibilité. Pour les applications qui sont démarrées de manière dynamique à l’aide de l’activation COM, la plupart n’ont aucun problème de compatibilité, car les autorisations de lancement doivent inclure déjà toute personne capable d’activer un objet. dans le cas contraire, de telles applications génèrent des échecs d’activation, même avant l’application de Windows XP SP2 ou Windows Server 2003 SP1, lorsque les appelants sans autorisation launch essaient d’activer un objet et que le serveur COM n’est pas déjà en cours d’exécution.

les applications les plus problématiques pour les problèmes de compatibilité sont les applications COM qui sont déjà démarrées par un autre mécanisme, comme Windows Explorer ou le gestionnaire de contrôle des services. Vous pouvez également démarrer ces applications à l’aide d’une activation COM précédente, qui remplace les autorisations d’accès et de lancement par défaut et spécifie des autorisations de lancement qui sont plus restrictives que les autorisations d’appel. Pour plus d’informations sur la résolution de ce problème de compatibilité, consultez « Comment faire résoudre ces problèmes ». dans la section suivante.

si un système qui est mis à niveau vers Windows XP SP2 ou Windows Server 2003 SP1 est restauré à un état antérieur, toute entrée de contrôle d’accès qui a été modifiée pour autoriser l’accès local, l’accès à distance, ou les deux, est interprétée pour autoriser l’accès local et distant. Toute entrée du contrôle d’accès qui a été modifiée pour refuser l’accès local, l’accès à distance, ou les deux, est interprétée pour refuser l’accès local et distant. Chaque fois que vous désinstallez un Service Pack, vous devez vous assurer qu’aucune ACE nouvellement définie ne provoque l’arrêt du fonctionnement des applications.

### <a name="how-do-i-resolve-these-issues"></a>Comment faire résoudre ces problèmes ?

Si vous implémentez un serveur COM et que vous remplacez les paramètres de sécurité par défaut, vérifiez que la liste de contrôle d’accès des autorisations de lancement spécifiques à l’application accorde l’autorisation d’activation aux utilisateurs appropriés. si ce n’est pas le cas, vous devez modifier votre liste de contrôle d’accès d’autorisation d’exécution propre à l’application pour accorder des droits d’activation aux utilisateurs appropriés afin que les applications et les composants de Windows qui utilisent DCOM n’échouent pas. Ces autorisations de lancement spécifiques à l’application sont stockées dans le registre.

Les listes de contrôle d’accès COM peuvent être créées ou modifiées à l’aide de fonctions de sécurité normales.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>quels sont les paramètres ajoutés ou modifiés dans Windows XP Service Pack 2 ?

> [!Caution]  
> une utilisation incorrecte de ces paramètres peut entraîner l’échec des applications et des composants de Windows qui utilisent DCOM.

 

Les abréviations suivantes sont utilisées dans le tableau suivant :

LL-lancement local

Activation de LA locale

RL-lancement à distance

RA-activation à distance

Appels d’accès LC-local

RC-appels d’accès à distance

Liste de Access Control ACL



| Nom du paramètre                                                                                         | Emplacement                                                                                                       | Valeur par défaut précédente                                                                                                                                                                     | Valeur par défaut                                                                                                                                                                                                                                                                                                                                                             | Valeurs possibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Tout le monde, LA, RL, RA<br/> Façon<br/> LL, LA, RL, RA<br/> (Il s’agit d’une nouvelle clé de registre. En fonction du comportement existant, il s’agit des valeurs effectives.)<br/> | Administrateur : LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Tout le monde-LC, RC<br/> Anonyme-LC, RC<br/> (Il s’agit d’une nouvelle clé de registre. En fonction du comportement existant, il s’agit des valeurs effectives.)<br/>                            | Tout le monde : LC, RC<br/> Anonyme : LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Non applicable.<br/>                                                                                                                                                                 | Cette clé de Registre n’est pas présente ; Toutefois, une clé ou une valeur manquante est interprétée comme 2.<br/> Cet événement n’est pas consigné par défaut. Si vous modifiez cette valeur sur 1 pour démarrer la journalisation de ces informations pour vous aider à résoudre un problème, veillez à surveiller la taille du journal des événements, car il s’agit d’un événement qui peut générer un grand nombre d’entrées.<br/> | 1-consigne toujours les échecs du journal des événements pendant un appel dans le processus serveur COM.<br/> 2-ne jamais enregistrer les échecs du journal des événements pendant un appel dans le processus du serveur d’appel.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Non applicable.<br/>                                                                                                                                                                 | Cette clé de Registre n’est pas présente ; Toutefois, une clé ou une valeur manquante est interprétée comme 1.<br/> Cet événement est consigné par défaut. Il doit rarement se produire.<br/>                                                                                                                                                                                                    | 1-enregistre toujours les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/> 2-ne jamais enregistrer les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/> |
| DCOM : restrictions de lancement d’ordinateur dans la syntaxe SDDL (Security Descriptor Definition Language)<br/> | (Objet stratégie de groupe) Configuration de l’ordinateur \\ Windows Paramètres les \\ stratégies locales \\ Options de sécurité<br/>  | Non applicable.<br/>                                                                                                                                                                 | Non défini<br/>                                                                                                                                                                                                                                                                                                                                                    | Liste de contrôle d’accès au format SDDL. L’existence de cette stratégie remplace les valeurs dans MachineLaunchRestriction, auparavant.<br/>                                                                                            |
| DCOM : restrictions d’accès à l’ordinateur dans la syntaxe SDDL (Security Descriptor Definition Language)<br/> | (Objet stratégie de groupe) Configuration de l’ordinateur \\ Windows Paramètres les \\ stratégies locales \\ Options de sécurité<br/> | Non applicable.<br/>                                                                                                                                                                 | Non défini<br/>                                                                                                                                                                                                                                                                                                                                                    | Liste de contrôle d’accès au format SDDL. L’existence de cette stratégie remplace les valeurs dans MachineAccessRestriction, auparavant.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Quels sont les paramètres qui ont été ajoutés ou modifiés dans Windows Server 2003 Service Pack 1 ?

> [!Note]  
> une utilisation incorrecte de ces paramètres peut entraîner l’échec des applications et des composants de Windows qui utilisent DCOM.

 

Les abréviations suivantes sont utilisées dans le tableau suivant :

LL-lancement local

Activation de LA locale

RL-lancement à distance

RA-activation à distance

Appels d’accès LC-local

RC-appels d’accès à distance

Liste de Access Control ACL



| Nom du paramètre                                                                                         | Emplacement                                                                                                       | Valeur par défaut précédente                                                                                                                                                             | Valeur par défaut                                                                                                                                                                                                                                                                                                                                                             | Valeurs possibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Tout le monde : LL, LA, RL, RA<br/> Anonyme : LL, LA, RL, RA<br/> (Il s’agit d’une nouvelle clé de registre. En fonction du comportement existant, il s’agit des valeurs effectives.)<br/> | Administrateur : LL, LA, RL, RA<br/> Tout le monde : LL, LA<br/> Utilisateurs du modèle COM distribué : LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Tout le monde : LC, RC<br/> Anonyme : LC, RC<br/> (Il s’agit d’une nouvelle clé de registre. En fonction du comportement existant, il s’agit des valeurs effectives.)<br/>                 | Tout le monde : LC, RC<br/> Anonyme : LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Non applicable.<br/>                                                                                                                                                         | Cette clé de Registre n’est pas présente ; Toutefois, une clé ou une valeur manquante est interprétée comme 2.<br/> Cet événement n’est pas consigné par défaut. Si vous modifiez cette valeur sur 1 pour démarrer la journalisation de ces informations pour vous aider à résoudre un problème, veillez à surveiller la taille du journal des événements, car il s’agit d’un événement qui peut générer un grand nombre d’entrées.<br/> | 1-enregistre toujours les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/> 2-ne jamais enregistrer les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Non applicable.<br/>                                                                                                                                                         | Cette clé de Registre n’est pas présente ; Toutefois, une clé ou une valeur manquante est interprétée comme 1.<br/> Cet événement est consigné par défaut. Il doit rarement se produire.<br/>                                                                                                                                                                                                    | 1-consigne toujours les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/> 2-ne jamais enregistrer les échecs du journal des événements lorsque l’infrastructure COM trouve un descripteur de sécurité non valide.<br/>         |
| DCOM : restrictions de lancement d’ordinateur dans la syntaxe SDDL (Security Descriptor Definition Language)<br/> | (Objet stratégie de groupe) Configuration de l’ordinateur \\ Windows Paramètres les \\ stratégies locales \\ Options de sécurité<br/> | Non applicable.<br/>                                                                                                                                                         | Non défini.<br/>                                                                                                                                                                                                                                                                                                                                                   | Liste de contrôle d’accès au format SDDL. L’existence de cette stratégie remplace les valeurs dans MachineLaunchRestriction, auparavant.<br/>                                                                                            |
| DCOM : restrictions d’accès à l’ordinateur dans la syntaxe SDDL (Security Descriptor Definition Language)<br/> | (Objet stratégie de groupe) Configuration de l’ordinateur \\ Windows Paramètres les \\ stratégies locales \\ Options de sécurité<br/> | Non applicable.<br/>                                                                                                                                                         | Non défini.<br/>                                                                                                                                                                                                                                                                                                                                                   | Liste de contrôle d’accès au format SDDL. L’existence de cette stratégie remplace les valeurs dans MachineAccessRestriction, auparavant.<br/>                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

