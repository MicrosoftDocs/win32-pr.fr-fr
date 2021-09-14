---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossaire COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915703"
---
# <a name="com-glossary"></a>Glossaire COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**jeton d’accès**
</dt> <dd>

Objet qui décrit le contexte de sécurité d’un processus ou d’un thread. Les informations contenues dans un jeton incluent l’identité et les privilèges du compte d’utilisateur associé au processus ou au thread. Lorsqu’un utilisateur ouvre une session, le système vérifie le mot de passe de l’utilisateur en le comparant avec les informations stockées dans une base de données de sécurité. Si le mot de passe est authentifié, le système génère un jeton d’accès. Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propriétés ACID**
</dt> <dd>

Acronyme de pionnier de traitement des transactions pour atomicité, cohérence, isolation et durabilité. Ces propriétés garantissent un comportement prévisible, renforçant le rôle des transactions en tant que propositions « tout ou rien » conçues pour fournir des résultats cohérents et prévisibles dans un environnement distribué lorsque des défaillances indépendantes peuvent se produire.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**actionne**
</dt> <dd>

Chaîne d’événements qui entraîne la création d’un objet COM et le retour d’un pointeur valide vers une interface sur cet objet. Dans COM+, un objet est activé soit dans son propre contexte, soit dans celui de son créateur (un objet qui a demandé l’objet en cours d’activation). Les services COM+ s’appuient sur l’activation appropriée d’un objet en fonction de la configuration de l’objet. Au cours de l’activation, le système détermine le contexte dans lequel l’objet s’exécute, initialise les propriétés de contexte, vérifie les autorisations d’accès et établit une identité de sécurité.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**sécurité d’activation**
</dt> <dd>

Forme de protection de sécurité qui détermine qui peut lancer un serveur. La sécurité d’activation est automatiquement appliquée par le gestionnaire de contrôle des services (SCM) d’un ordinateur particulier. Lors de la réception d’une demande d’activation d’un objet par un client, le SCM vérifie la demande par rapport aux informations d’activation de sécurité stockées dans son registre. La sécurité d’activation est également vérifiée pour les activations du même ordinateur. Également appelé *lancement sécurité*.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**type d’activation**
</dt> <dd>

Catégorie d’activation pour une application COM+ qui indique si l’application s’exécute dans ou en dehors de l’espace de processus de son client (selon qu’il s’agit d’une application de bibliothèque ou de serveur, respectivement) et si l’application s’exécute en tant que service.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**bas**
</dt> <dd>

Dans COM+, il s’agit d’un thread logique comprenant une ou plusieurs transactions et contenant une collection de composants regroupés dans une application COM+. Chaque objet COM appartient à une activité. L’association entre un objet et une activité ne peut pas être modifiée.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processus de modèle cloisonné**
</dt> <dd>

Processus qui a au moins deux cloisonnements à thread unique et aucun cloisonnement multithread.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy d’application**
</dt> <dd>

Ensemble de fichiers contenant des informations d’inscription permettant à un client d’accéder à distance à une application serveur COM+. Lorsqu’il est installé sur un ordinateur client, un fichier de proxy d’application écrit les informations relatives à l’application serveur sur l’ordinateur client. le client peut ensuite accéder à distance à l’application serveur.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**identification**
</dt> <dd>

Le processus de sécurité consistant à déterminer qu’un appelant d’une application est réellement celui qu’il dit, c’est qu’il vérifie l’authenticité d’une revendication d’identité. Pour les applications COM+, l’authentification peut être activée et configurée de manière administrative, après quoi elle fonctionne de façon transparente pour l’application.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**l'**
</dt> <dd>

Processus de sécurité permettant de déterminer si un appelant d’une application est autorisé à faire ce qu’il demande.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**mise en cache de Resource Manager**
</dt> <dd>

Gestionnaire de ressources qui agit comme serveur frontal d’un autre gestionnaire de ressources et qui met en cache les informations localement, ce qui réduit le coût d’accès à la ressource sous-jacente. Contrairement à un gestionnaire de ressources conventionnel, un gestionnaire de ressources de mise en cache ne participe pas à la récupération car il ne stocke jamais de manière permanente les données sous-jacentes.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**sécurité de l’appel**
</dt> <dd>

Forme de protection de sécurité qui permet de contrôler l’accès aux méthodes d’un objet serveur après le lancement d’un serveur.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**classe (COM)**
</dt> <dd>

Implémentation concrète nommée d’une ou de plusieurs interfaces. Une classe COM est identifiée par un CLSID et, parfois, un ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**masquer**
</dt> <dd>

Possibilité pour un serveur de masquer sa propre identité lors d’appels au nom d’un client. Lorsque le masquage est activé, les appels effectués par le serveur qui emprunte l’identité du client peuvent être effectués sous l’identité du client. Lorsque le masquage est désactivé, les appels par le serveur sont effectués sous l’identité du serveur.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Application COM+**
</dt> <dd>

Unité principale d’administration et de sécurité pour les services de composants. Une application COM+ est un groupe de composants COM qui exécutent généralement des fonctions associées. Ces composants se composent davantage d’interfaces et de méthodes COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Regroupement d’applications COM+**
</dt> <dd>

Fonctionnalité services de composants qui permet la mise à l’échelle des processus à thread unique et peut également vous aider à récupérer après des défaillances dans les processus uniques en fournissant d’autres processus en cours d’exécution capables de gérer les activations.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Recyclage des applications COM+**
</dt> <dd>

Fonctionnalité services de composants qui augmente considérablement la stabilité globale de vos applications en vous permettant d’arrêter en douceur un processus associé à une application et de la redémarrer.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catalogue COM+** 
</dt> <dd>

Magasin de données qui contient les données de configuration COM+. Les performances des tâches d’administration COM+ nécessitent la lecture et l’écriture des données stockées dans le catalogue. Le catalogue est accessible uniquement par le biais de l’outil d’administration Services de composants ou par le biais de la bibliothèque comadmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Événements COM+**
</dt> <dd>

Les événements COM+ correspondent aux serveurs de publication et aux abonnés et les connecte à l’aide d’un système d’événements faiblement couplés. Un serveur de publication effectue l’appel de méthode pour initier un événement, et un abonné reçoit ces appels via le système d’événements plutôt que directement à partir du serveur de publication. Le service événements COM+ gère la liste des abonnés intéressés qui reçoivent les appels et dirige ces appels sans avoir besoin de connaître le serveur de publication.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Application de bibliothèque COM+**
</dt> <dd>

Application COM+ qui s’exécute dans le processus du client qui la crée. Les applications de bibliothèque peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Mise en pool d’objets COM+**
</dt> <dd>

Service automatique fourni par COM+ qui vous permet de configurer un composant pour que des instances de lui-même restent actives dans un pool, prêtes à être utilisées par n’importe quel client qui demande le composant.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partitions COM+**
</dt> <dd>

Service COM+ qui permet, sur un seul ordinateur, de créer des espaces d’exécution distincts pour les applications.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Jeux de partitions COM+**
</dt> <dd>

Groupe de partitions COM+ mappé à un ID d’utilisateur particulier dans Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Composants en file d’attente COM+**
</dt> <dd>

Service COM+, basé sur Microsoft Message Queuing, qui offre un moyen simple d’appeler et d’exécuter des composants de manière asynchrone. Le traitement des messages peut se produire sans tenir compte de la disponibilité ou de l’accessibilité de l’expéditeur ou du destinataire.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Application serveur COM+**
</dt> <dd>

Application COM+ qui s’exécute dans son propre processus. Les applications serveur peuvent prendre en charge tous les services COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**
</dt> <dd>

Fonctionnalité services de composants qui vous permet d’exposer une application COM+ en tant que service Web XML. Le protocole SOAP COM+ vous permet également d’utiliser un service Web XML en tant que composant COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Composant COM**
</dt> <dd>

Unité binaire de code qui comprend le code d’empaquetage et d’inscription et qui crée des objets COM. Toutes les applications COM+ comportent un ou plusieurs composants COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**arborescence de validation**
</dt> <dd>

Dans un système de transactions distribuées, la représentation conceptuelle d’une transaction est basée sur les relations hiérarchiques entre les gestionnaires de transactions individuels participant à une transaction distribuée. Les gestionnaires de ressources inscrits dans cette hiérarchie sont associés aux gestionnaires de transactions.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objet COM**
</dt> <dd>

Dans le modèle de programmation COM, structure de programmation encapsulant à la fois les données et les fonctionnalités, qui sont définies et allouées en tant qu’unité unique et pour lesquelles le seul accès public s’effectue via les interfaces de la structure de programmation. Un objet COM doit prendre en charge, au minimum, l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , qui maintient l’existence de l’objet pendant son utilisation et fournit l’accès aux autres interfaces de l’objet.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gestionnaire des ressources de compensation (CRM)**
</dt> <dd>

Fonctionnalité COM+ qui permet aux ressources non transactionnelles de participer à une transaction de validation en deux phases avec le Distributed Transaction Coordinator Microsoft (DTC). En règle générale, les gestionnaires de ressources ne fournissent pas les fonctionnalités d’isolation des gestionnaires de ressources complets, mais ils fournissent une atomicité et une durabilité transactionnelles en écrivant dans un journal.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Outil d’administration Services de composants**
</dt> <dd>

Composant logiciel enfichable d’interface utilisateur permettant aux administrateurs et aux développeurs de créer, de configurer et de gérer des applications COM+, ainsi que d’administrer les transactions distribuées et les bases de données résidant en mémoire. L’outil d’administration Services de composants peut également être utilisé pour afficher des événements système et gérer des services système locaux sur l’ordinateur sur lequel l’outil est installé.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modèle conceptuel**
</dt> <dd>

La première étape de la phase de conception de l’application COM+, où le développeur définit les problèmes d’entreprise à résoudre et détermine les composants et services requis.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**d’accès concurrentiel**
</dt> <dd>

Capacité de plusieurs transactions ou processus à accéder aux mêmes données en même temps. COM+ gère généralement l’accès concurrentiel par le biais de la synchronisation.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**composant configuré**
</dt> <dd>

Composant COM qui a été installé dans une application COM+. Une fois installé, le composant est configuré dans le catalogue COM+ pour utiliser les services COM+ disponibles.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contexte**
</dt> <dd>

Ensemble de propriétés au moment de l’exécution associées à un ou plusieurs objets COM utilisés pour fournir des services pour ces objets. Chaque objet COM s’exécute dans un contexte unique de l’activation à la désactivation (toujours dans le même cloisonnement). Initialisé lorsqu’un objet est activé, les propriétés de contexte, telles que les propriétés de contexte de sécurité, représentent les besoins d’un objet au moment de l’exécution.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**couche données**
</dt> <dd>

Dans le modèle d’architecture à trois niveaux pour les applications d’entreprise, la couche d’accès au SGBD, accessible par le biais du niveau intermédiaire ou de la couche des services d’entreprise, et à l’occasion de la couche présentation ou de la couche services utilisateur. La couche données se compose de composants d’accès aux données (plutôt que de connexions SGBD brutes) pour faciliter le partage des ressources et permettre la configuration des clients sans installer les bibliothèques SGBD et les pilotes ODBC sur chaque client. Également appelée *couche des services de données*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Fatal**
</dt> <dd>

Dans les applications multithread, problème de threading qui se produit lorsque chaque membre d’un ensemble de threads attend un autre membre de l’ensemble.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**délégation**
</dt> <dd>

Forme d’emprunt d’identité qui autorise un serveur à agir au nom d’un client, ce qui permet au serveur d’emprunter l’identité de clients sur le réseau.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transaction distribuée**
</dt> <dd>

Transaction impliquant plusieurs gestionnaires de ressources, qui peuvent se trouver sur des ordinateurs identiques ou différents.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**
</dt> <dd>

Service système qui gère les transactions et les communications liées aux transactions qui sont réparties sur deux ou plusieurs gestionnaires de ressources sur un ou plusieurs systèmes afin de garantir des transactions ACID correctes.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**masquage dynamique**
</dt> <dd>

Forme de masquage où l’identité du client d’origine est détectée comme jeton d’accès au thread du serveur sur chaque appel de méthode au serveur en aval. Bien que l’identité présentée puisse être déterminée dynamiquement, la surcharge requise pour le faire peut être considérablement plus coûteuse. Pour les applications COM+, la configuration par défaut est pour la fonctionnalité de voilage dynamique, car elle offre la flexibilité qui est généralement requise dans les circonstances qui nécessitent l’utilisation de l’emprunt d’identité en premier lieu.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objet Enumerator**
</dt> <dd>

Permet l’énumération des éléments dans une collection.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**événement**
</dt> <dd>

Action reconnue par un objet, par exemple en cliquant sur la souris ou en appuyant sur une touche, et pour laquelle vous pouvez écrire du code pour répondre.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Event, objet de classe**
</dt> <dd>

Composant configuré qui fournit un enregistrement persistant dans le système d’événement COM+ pour décrire les serveurs de publication et les interfaces de déclenchement associées à ces serveurs de publication.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**méthode d’événement**
</dt> <dd>

Méthode dans une interface COM+ qui identifie un événement COM+. Les méthodes d’événement doivent être nommées de manière unique et ne peuvent contenir que des paramètres d’entrée. La valeur de retour doit être un **HRESULT**.

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objet d’événement**
</dt> <dd>

Objet COM qui peut signaler un ou plusieurs threads qu’un événement s’est produit. Tout thread dans un processus peut créer un objet d’événement.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**titre**
</dt> <dd>

Condition ou erreur anormale qui se produit pendant l’exécution d’un programme et qui requiert l’exécution de logiciels en dehors du déroulement normal du contrôle.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**échec**
</dt> <dd>

Dans un système réseau en cluster, processus de déplacement d’une ressource surchargée ou ayant échoué (par exemple, un serveur, un lecteur de disque ou un réseau) vers son composant de sauvegarde.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processus à threads libres**
</dt> <dd>

Processus qui a un cloisonnement multithread et aucun cloisonnement à thread unique.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**coordinateur de validation globale**
</dt> <dd>

sur un système de transactions distribuées basé sur Microsoft Windows, le gestionnaire de transactions racine de l’arborescence de validation. Ce coordinateur prend la décision de valider ou d’abandonner une transaction donnée et n’est jamais incertaine.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**emprunt d’identité**
</dt> <dd>

Capacité d’un thread à s’exécuter dans un contexte de sécurité différent de celui du processus propriétaire du thread. Le thread serveur utilise un jeton d’accès qui représente les informations d’identification du client et, avec cela, il peut accéder aux ressources auxquelles le client peut accéder.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**niveau d’emprunt d’identité**
</dt> <dd>

Paramètre utilisé par le client pour accorder au serveur un niveau d’autorité particulier pour effectuer des actions au nom du client. Dans COM+, cette valeur ne peut être définie que pour les applications serveur COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**
</dt> <dd>

Pour un objet activé dans un contexte donné, processus de gestion des appels à cet objet à partir de la limite du contexte. Les appels à travers le contexte sont gérés avec des proxies d’interface légère qui gèrent la médiation requise pour ajuster l’environnement d’exécution à partir d’un qui prend en charge l’appelant sur un autre qui prend en charge l’appelé.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**
</dt> <dd>

Dans la programmation COM, collection de fonctions publiques associées qui fournissent l’accès à un objet COM. L’ensemble d’interfaces sur un objet COM compose un contrat qui spécifie comment les programmes et d’autres objets peuvent interagir avec l’objet COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy d’interface**
</dt> <dd>

Objet spécifique à l’interface qui empaquette (marshale) les paramètres de cette interface en préparation d’un appel de méthode distant et décompresse (démarshale) les valeurs de retour du stub d’interface. Un proxy s’exécute dans l’espace d’adressage de l’expéditeur et communique avec un stub correspondant dans l’espace d’adressage du destinataire.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**stub d’interface**
</dt> <dd>

Objet spécifique à l’interface qui décompresse les paramètres marshalés, appelle la méthode requise, et les packages (Marshalers) retournent des valeurs à partir de la méthode appelée. Le stub s’exécute dans l’espace d’adressage du destinataire et communique avec un proxy d’interface correspondant dans l’espace d’adressage de l’expéditeur.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**Objet Interior**
</dt> <dd>

Dans une hiérarchie transactionnelle, tout objet sous l’objet racine.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**activation juste-à-temps (JIT)**
</dt> <dd>

Service automatique fourni par COM+ qui autorise l’utilisation plus productive des ressources serveur inactives. Lorsqu’un composant est configuré en tant que JIT activé, COM+ peut désactiver une instance de celui-ci lorsqu’un client contient encore une référence active à l’objet. La prochaine fois que le client appelle une méthode sur l’objet, COM+ réactivera l’objet en toute transparence au client, juste à temps.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**composant hérité**
</dt> <dd>

Composant non configuré qui a été installé dans une application COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**écouteur**
</dt> <dd>

Élément architectural du service de composants en file d’attente COM+. L’écouteur est un objet COM qui ouvre la file d’attente de messages associée à son application hôte et attend l’arrivée de messages. À mesure que les messages arrivent, l’écouteur distribue les threads qui traitent les messages.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modèle logique**
</dt> <dd>

Deuxième étape d’un processus de conception d’application COM+, où le modèle conceptuel est divisé en niveaux logiques de l’architecture à trois niveaux, comme suit : la couche présentation, ou les services utilisateur ; la couche intermédiaire, ou services professionnels ; et la couche données, ou services de données.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**événement faiblement couplé**
</dt> <dd>

Événement dont l’expéditeur (éditeur) et le récepteur (abonné) ne sont pas étroitement liés. Dans un système d’événement faiblement couplé, tel que les événements COM+, les informations d’événements provenant de différents serveurs de publication sont conservées dans un magasin d’événements. Les abonnés interrogent ce magasin et sélectionnent les événements qu’ils souhaitent recevoir. La sélection des informations d’événement dans le magasin d’événements crée un abonnement. Lorsqu’un événement se produit, le système d’événements recherche dans cette base de données et recherche les abonnés intéressés, crée un nouvel objet de chaque classe intéressée et appelle une méthode sur cet objet.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**
</dt> <dd>

Processus d’empaquetage et d’empaquetage des paramètres de méthode d’interface à travers les limites de thread ou de processus pour qu’un appel de procédure distante puisse avoir lieu.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message Mover**
</dt> <dd>

Élément architectural du service de composants en file d’attente COM+ qui déplace les messages ayant échoué vers leur file d’attente d’entrée pour qu’ils puissent être retentés.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**événement méta**
</dt> <dd>

Type d’événement utilisé par le système d’événements COM+ pour notifier les abonnés intéressés chaque fois que des objets de classe d’événements ou des abonnements sont créés, modifiés ou supprimés.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**méthode**
</dt> <dd>

Dans la programmation COM, processus effectué par un objet COM lorsqu’il reçoit un message.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**niveau intermédiaire**
</dt> <dd>

Dans le modèle d’architecture à trois niveaux pour les applications d’entreprise, la couche comprenant la logique métier et les règles de données. Les composants qui composent la couche intermédiaire peuvent être utilisés pour appliquer des règles d’entreprise, telles que des algorithmes métier, des réglementations juridiques ou gouvernementales, et des règles de données, qui sont conçues pour maintenir la cohérence des structures de données dans des bases de données spécifiques ou multiples. Étant donné que ces composants de couche intermédiaire ne sont pas liés à un client spécifique, ils peuvent être utilisés par toutes les applications et peuvent être déplacés vers différents emplacements en fonction du temps de réponse et que d’autres règles requièrent. Également appelée *couche de services d’entreprise* ou *couche de logique métier*.

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processus de modèle mixte**
</dt> <dd>

Processus qui a un cloisonnement multithread et un ou plusieurs cloisonnements à thread unique.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Nom qui identifie de façon unique un objet COM. De la même façon qu’un chemin d’accès identifie un fichier dans le système de fichiers, un moniker identifie un objet COM dans l’espace de noms du répertoire.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**Fichier.msi**
</dt> <dd>

Fichier créé par l’outil d’administration Services de composants lorsque vous exportez une application COM+ ou un proxy d’application pour l’installation sur un autre ordinateur. le fichier .msi peut être installé sur n’importe quel client Windows utilisant Windows Installer.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modèle multithread cloisonné**
</dt> <dd>

Modèle Apartment dans lequel tous les threads du processus qui ont été initialisés en tant que threads libres résident dans un seul cloisonnement. Par conséquent, il n’est pas nécessaire d’effectuer un marshaling entre les threads. Les threads n’ont pas besoin de récupérer et de distribuer les messages, car COM n’utilise pas les messages de fenêtre dans ce modèle.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transaction imbriquée**
</dt> <dd>

Une transaction secondaire lancée à partir d’une limite de transaction primaire ou parente existante. La transaction principale n’est pas validée tant que toutes ses transactions subordonnées ou imbriquées ne sont pas validées. COM+ ne prend pas en charge les transactions imbriquées.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modèle de cloisonnement neutre**
</dt> <dd>

Modèle de thread dans lequel les objets suivent les instructions pour les cloisonnements multithread, mais peuvent s’exécuter sur n’importe quel type de thread. Le modèle de cloisonnement neutre est le modèle de thread recommandé pour les composants COM et les applications COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objet persistant**
</dt> <dd>

Objet COM qui peut enregistrer son état interne lorsqu’il y est invité par un client et qui est conforme aux normes définies par COM par le biais desquelles les clients peuvent demander l’initialisation, le chargement et l’enregistrement d’objets dans un magasin de données (par exemple, un fichier plat, un stockage structuré ou la mémoire). Il incombe au client de gérer l’emplacement où les données persistantes de l’objet sont stockées, mais pas le format des données.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interface d’objet persistant**
</dt> <dd>

Interface COM implémentée par un objet persistant. Les clients utilisent des interfaces d’objets persistants pour indiquer à ces objets persistants quand et où stocker leur état.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interface de notification de phase zéro**
</dt> <dd>

Interface COM+ qui permet aux applications de détecter lorsqu’une transaction est prête à passer à un protocole de validation en deux phases afin de pouvoir effectuer les opérations de notification nécessaires et communiquer avec le gestionnaire de transactions lorsque les opérations sont terminées.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modèle physique**
</dt> <dd>

Troisième et dernière étape du processus de conception de l’application COM+, où le développeur détermine où les composants résident physiquement et comment ils doivent être codés.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**lecteur**
</dt> <dd>

Élément architectural du service de composants en file d’attente COM+ qui récupère le message à partir d’une file d’attente, puis charge l’objet serveur et les stubs d’interface standard pour démarshaler les données et appeler les méthodes serveur. Le lecteur démarshale le contexte de sécurité du client côté serveur, puis appelle le composant serveur et effectue les mêmes appels de méthode. Les appels de méthode ne sont pas lus par le joueur jusqu’à ce que le composant client se termine et que la transaction qui a enregistré la méthode appelle valids.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**niveau de présentation**
</dt> <dd>

Dans le modèle d’architecture à trois niveaux pour les applications métier, couche qui présente les données à l’utilisateur et permet éventuellement la manipulation de données et l’entrée de données. Les deux principaux types d’interface utilisateur pour la couche présentation sont l’application traditionnelle et l’application Web. Également appelée *couche des services utilisateur*.

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**jeton d’accès principal**
</dt> <dd>

Décrit le contexte de sécurité du compte d’utilisateur associé à un processus.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**gestionnaire proxy**
</dt> <dd>

Dans le marshaling standard, composant qui gère tous les proxies d’interface pour un seul objet.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**Pseudo-objet**
</dt> <dd>

Type d’objet contenu, tel qu’une sélection d’utilisateur dans un document, une plage de cellules dans une feuille de calcul ou une plage de caractères dans un document texte. Ce type d’objet est appelé Pseudo-objet, car il n’est pas traité comme un objet distinct tant qu’un utilisateur n’a pas marqué la sélection.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publication**
</dt> <dd>

Expéditeur d’un événement. Dans l’architecture des événements COM+, le serveur de publication effectue l’appel de méthode pour initialiser un événement.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker de file d’attente**
</dt> <dd>

Moniker utilisé pour activer un composant mis en file d’attente.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condition de concurrence critique**
</dt> <dd>

Dans une application multithread, condition qui se produit lorsque plusieurs threads accèdent à un élément de données sans coordination, ce qui peut entraîner des résultats incohérents, selon le thread qui atteint d’abord l’élément de données. COM fournit certaines fonctions spécifiquement conçues pour éviter les conditions de concurrence dans les serveurs hors processus.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**grave**
</dt> <dd>

Élément architectural du service de composants en file d’attente COM+ qui marshale le contexte de sécurité du client en message et enregistre tous les appels de méthode pour un objet. L’enregistreur est un gestionnaire proxy fourni par le système qui sélectionne les interfaces à partir des interfaces de mise en file d’attente dans le catalogue COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**distributeur de ressources**
</dt> <dd>

Dans le modèle de programmation COM+, composant qui gère l’état partagé non durable pour le compte des composants d’application au sein d’un processus. Les distributeurs de ressources sont similaires aux gestionnaires de ressources, mais sans garantie de durabilité.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Gestionnaire de ressources**
</dt> <dd>

Service qui gère les données persistantes ou durables dans les bases de données, les files d’attente de messages durables ou les systèmes de fichiers transactionnels. Il s’agit du gestionnaire de ressources qui sait comment stocker des données et effectuer une récupération d’urgence. Les applications serveur COM+ utilisent des gestionnaires de ressources pour maintenir l’État durable d’une application, par exemple l’enregistrement d’un inventaire, les commandes en attente et les comptes clients. Les gestionnaires de ressources travaillent en collaboration avec le Distributed Transaction Coordinator Microsoft (DTC) pour garantir l’atomicité et l’isolation à une application.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**sécurité basée sur les rôles**
</dt> <dd>

Service de sécurité COM+ fourni pour les applications COM+. Un rôle représente une catégorie d’utilisateurs définie pour une application COM+ en vue de déterminer les autorisations d’accès aux ressources de l’application. Les rôles sont assignés par un développeur à des composants, des interfaces et des méthodes. Les utilisateurs sont affectés par un administrateur aux rôles appropriés, ce qui permet à un utilisateur d’un rôle donné d’accéder à toutes les ressources auxquelles ce rôle est attribué.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objet racine**
</dt> <dd>

Le premier objet d’une transaction, appelé la racine de la transaction, est toujours placé dans une nouvelle limite transactionnelle. Il ne peut y avoir qu’un seul objet racine dans une transaction. Tous les autres objets de la hiérarchie transactionnelle sous l’objet racine sont appelés objets intérieurs.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Gestionnaire de transactions racine**
</dt> <dd>

Gestionnaire de transactions du système qui initie une transaction. La transaction n’est pas finalisée tant que le gestionnaire de transactions racine n’a pas déterminé l’état de la transaction (validé ou abandonné).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**sémaphore**
</dt> <dd>

Objet de noyau utilisé pour arbitrer l’accès à une ressource partagée.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Gestionnaire de contrôle des services (SCM)**
</dt> <dd>

un processus Microsoft Windows server qui gère tous les services du registre Windows.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gestionnaire de propriétés partagées (SPM)**
</dt> <dd>

Dans com+, un distributeur de ressources que vous pouvez utiliser pour partager un État non persistant entre plusieurs objets au sein d’un processus serveur.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processus monothread**
</dt> <dd>

Processus qui se compose d’un seul thread cloisonné, qui, à son tour, est constitué d’un seul thread. Tous les objets COM qui résident dans un cloisonnement à thread unique peuvent recevoir des appels de méthode à partir du seul thread qui appartient à ce cloisonnement.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**
</dt> <dd>

Protocole simple basé sur XML permettant d’échanger des informations structurées et de type sur le Web. Le protocole ne contient aucune sémantique d’application ou de transport, ce qui le rend hautement modulaire et extensible.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**fractionner l’inscription**
</dt> <dd>

pour les composants qui sont déjà des composants com existants et qui sont utilisés dans l’environnement des services com+, la disposition d’inscription dans laquelle l’aspect COM de base de l’inscription est stocké dans le registre Windows et les nouveaux services et attributs com+ (par exemple, les composants en file d’attente) sont stockés dans la base de données d’inscription com+. chaque attribut de composant est stocké dans le registre Windows ou la base de données d’inscription COM+. les nouveaux composants COM sont inscrits exclusivement dans la base de données d’inscription COM+, avec une certaine duplication dans le registre Windows pour que les outils existants puissent les utiliser.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**avec état**
</dt> <dd>

D’un système ou d’un processus qui surveille tous les détails de l’état d’une activité à laquelle il participe.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sans état**
</dt> <dd>

D’un système ou d’un processus qui participe à l’activité sans surveiller tous les détails de son état.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**masquage statique**
</dt> <dd>

Forme de masquage où l’identité du client d’origine peut être présentée une seule fois à un serveur en aval, en définissant l’identité du client d’origine une seule fois sur le proxy. Cette identité cliente est présentée sous la forme d’un jeton de thread de serveur qui sera utilisé lors des appels de méthode suivants.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**côté**
</dt> <dd>

Récepteur d’un événement. Dans l’architecture des événements COM+, l’abonné reçoit les appels émis par le serveur de publication.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objet d’abonnement**
</dt> <dd>

Dans le système d’événements COM+, objet créé par un abonné pour demander et gérer la remise des événements.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronisationméthode**
</dt> <dd>

Dans COM+, service qui passe du composant au composant et interdit à plusieurs appelants d’entrer le composant à un moment donné. La synchronisation détermine quand les threads peuvent distribuer des appels à un objet.

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modèle architectural à trois niveaux**
</dt> <dd>

L’infrastructure fondamentale pour le modèle de conception logique, segmente les composants d’une application en trois niveaux de services comme suit : la couche présentation, ou les services utilisateur ; la couche intermédiaire, ou services professionnels ; et la couche données, ou services de données. Ces niveaux ne correspondent pas nécessairement à des emplacements physiques sur différents ordinateurs sur un réseau, mais plutôt à des couches logiques de l’application.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**événement étroitement couplé**
</dt> <dd>

Événement dont l’expéditeur (éditeur) et le récepteur (abonné) sont étroitement liés. Dans un système d’événements étroitement couplé, le serveur de publication est fourni avec une interface sur laquelle appeler une méthode quand une modification se produit. L’abonné sait à partir de quel éditeur demander une notification et les interfaces qui sont exposées. Un système d’événements étroitement couplé nécessite que le serveur de publication et l’abonné s’exécutent à tout moment.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Journal des traces**
</dt> <dd>

Fichier journal généré automatiquement par le Distributed Transaction Coordinator Microsoft qui affiche les données relatives à une ou plusieurs transactions distribuées. Des exemples de données dans un journal des traces sont l’ID de transaction, le temps de transaction et les messages indiquant le résultat de la transaction.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**libellé**
</dt> <dd>

Unité de travail dans laquelle une série d’opérations connexes se produisent pendant un processus d’application. Une transaction s’exécute exactement une fois et est atomique : soit la totalité du travail est effectuée, soit aucune d’entre elles n’est.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocole Internet de transaction (TIP)**
</dt> <dd>

Transaction Internet Protocol est un protocole de validation en deux phases standard qui permet aux gestionnaires de transactions hétérogènes de coordonner les transactions distribuées, en particulier sur Internet. Le protocole de validation en deux phases TIP est simple à implémenter et est indépendant du protocole de communication entre applications, de sorte qu’il peut être utilisé avec n’importe quel protocole d’application, en particulier HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Gestionnaire de transactions**
</dt> <dd>

Partie du Distributed Transaction Coordinator Microsoft (DTC) qui s’exécute sur chaque ordinateur participant à une transaction distribuée et qui gère les activités liées à la validation ou à l’abandon de cette partie de la transaction.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**application de traitement des transactions**
</dt> <dd>

Collection d’opérations de transaction qui automatisent une tâche d’entreprise donnée.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**système de traitement des transactions**
</dt> <dd>

Système complet, comprenant à la fois le matériel et les logiciels de l’ordinateur, qui héberge une application de traitement des transactions pour effectuer des transactions de routine nécessaires pour mener à bien l’entreprise.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocole de validation en deux phases**
</dt> <dd>

Un protocole utilisé uniquement dans les transactions distribuées garantit que le résultat d’une transaction est cohérent dans l’ensemble des gestionnaires de transactions participant à la transaction. Le protocole fonctionne en deux phases distinctes pour valider ou abandonner une transaction : la phase 1 évalue la condition de chaque gestionnaire de ressources et la phase 2 termine la transaction.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**composant non configuré**
</dt> <dd>

Composant COM qui n’a pas été configuré dans le catalogue COM+. Les composants non configurés ne peuvent pas utiliser les services COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**déplacement**
</dt> <dd>

Pour les transactions DTC, structure de données opaque qui représente l’adresse du gestionnaire de transactions du gestionnaire de ressources.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**
</dt> <dd>

Ensemble standard d’interfaces de programmation qui permettent aux développeurs d’applications COM+ d’accéder aux bases de données compatibles XA et de créer des gestionnaires de ressources qui fonctionnent avec les bases de données relationnelles, la mise en file d’attente des messages, les fichiers transactionnels et les bases de données orientées objet. Bien que Microsoft ne prenne pas directement en charge le protocole XA, Microsoft prend en charge les fonctions de traduction entre les transactions OLE et XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Services Web XML**
</dt> <dd>

Unités de logique d’application fournissant des données et des services à d’autres applications. Les applications accèdent aux services Web XML via des protocoles Web standard, tels que SOAP.

</dd> </dl>

 

 
