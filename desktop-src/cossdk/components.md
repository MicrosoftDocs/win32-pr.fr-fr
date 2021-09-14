---
description: Contient un objet pour chaque composant de l’application associée.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Collection de composants
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291842"
---
# <a name="components-collection"></a>Collection de composants

Contient un objet pour chaque composant de l’application associée. La collection de **composants** est toujours liée à un objet dans la collection d' [**applications**](applications.md) . Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.

Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membres

La collection **Components** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Applications**](applications.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [Nombre de bits](#bitness)
-   [IDENTIFICATEUR](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [ConstructorString](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [Description](#description)
-   [DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [ExceptionClass](#exceptionclass)
-   [FireInParallel](#fireinparallel)
-   [IISIntrinsics](#iisintrinsics)
-   [InitializeServerApplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [IsEventClass](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [IsPrivateComponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [MultiInterfacePublisherFilterCLSID](#multiinterfacepublisherfilterclsid)
-   [MustRunInClientContext](#mustruninclientcontext)
-   [MustRunInDefaultContext](#mustrunindefaultcontext)
-   [ObjectPoolingEnabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [SoapAssemblyName](#soapassemblyname)
-   [SoapTypeName](#soaptypename)
-   [Synchronisation](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [Transaction](#componenttransactiontimeout)
-   [TxIsolationLevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [VersionSubBuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>AllowInprocSubscribers



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------|
| Description    | Active les abonnés au processus si le composant est une classe d’événements. |
| Access         | Lecture/écriture                                                          |
| Type           | Bool                                                               |
| Default        | Vrai                                                               |
| Système minimal | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID de l’application contenant le composant. Doit être un GUID d’application valide, qui est vérifié avant l’appel de [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) . Si cette valeur est remplacée par un GUID pour une autre application, le composant se déplace vers cette application. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                        |
| Type           | String                                                                                                                                                                                                                                                                                           |
| Valeur par défaut        | N/A                                                                                                                                                                                                                                                                                              |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Nombre de bits



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Représente le type de bits binaire d’un composant. sur les systèmes qui utilisent la Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits. |
| Access         | Lecture seule                                                                                                                                                            |
| Type           | Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                       |
| Default        | N/A                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID du composant. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Valeur par défaut        | N/A                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique si les contrôles d’accès basés sur les rôles sont effectués sur les appels au composant et fonctionnent conjointement avec les propriétés AccessChecksLevel et ApplicationAccessChecksEnabled de l’application. |
| Access         | Lecture/écriture                                                                                                                                                                                                  |
| Type           | Bool                                                                                                                                                                                                       |
| Default        | False                                                                                                                                                                                                      |
| Système minimal | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | En cas d’utilisation dans une transaction, spécifie la période pendant laquelle ce composant provoque l’expiration du délai d’attente de la transaction. La valeur par défaut est 60 secondes et ne peut pas dépasser 3600 secondes (1 heure). La valeur du délai d’attente peut être définie sur 0, en spécifiant un délai d’expiration de transaction infini. Pour que cette propriété soit utilisée, ComponentTransactionTimeoutEnabled doit avoir la valeur true. La valeur de cette propriété remplace le délai d’expiration de la transaction globale spécifié par la propriété TransactionTimeout de la collection [**LocalComputer**](localcomputer.md) . |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Type           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Default        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Spécifie si le délai d’expiration de la transaction est activé pour ce composant. Par défaut, la fonctionnalité de délai d’expiration de la transaction est désactivée. Lorsque cette propriété a la valeur true, le délai d’attente spécifié par ComponentTransactionTimeout est utilisé. Lorsque cette propriété a la valeur false, le délai d’attente spécifié par la propriété TransactionTimeout de la collection [**LocalComputer**](localcomputer.md) est utilisé. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                      |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Default        | False                                                                                                                                                                                                                                                                                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Permet de passer des propriétés de contexte du COM Transaction Integrator (COMTI) dans le contexte de cette classe. Le composant COMTI facilite l’encapsulation des transactions de macroordinateurs et de la logique métier en tant que composants COM. |
| Access         | Lecture/écriture                                                                                                                                                                                                            |
| Type           | Bool                                                                                                                                                                                                                 |
| Default        | False                                                                                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------|
| Description    | Détermine si le ConstructorString est passé à l’objet lors de sa construction. |
| Access         | Lecture/écriture                                                                                |
| Type           | Bool                                                                                     |
| Default        | False                                                                                    |
| Système minimal | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>ConstructorString



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne d’initialisation pour la construction du composant. Vous pouvez créer différents objets à partir du même composant générique en utilisant des chaînes de constructeur d’objet. Si ConstructionEnabled a la valeur false, cette propriété est ignorée. |
| Access         | Lecture/écriture                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                             |
| Valeur par défaut        | ""                                                                                                                                                                                                                 |
| Système minimal | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de la création de l’objet, nombre de millisecondes avant qu’une erreur de délai d’attente soit renvoyée. Le délai d’expiration maximal est de 2147483647 millisecondes (environ 25 jours). |
| Access         | Lecture/écriture                                                                                                                                              |
| Type           | Long (0-2147483647)                                                                                                                                    |
| Default        | 0                                                                                                                                                      |
| Système minimal | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|--------------------------|
| Description    | Décrit le composant. |
| Access         | Lecture/écriture                |
| Type           | String                   |
| Valeur par défaut        | ""                       |
| Système minimal | Windows 2000             |



 

### <a name="dll"></a>DLL



| Entrée | Valeur |
|----------------|---------------------------------------------------------|
| Description    | Nom et chemin d’accès du fichier contenant le composant. |
| Access         | Lecture seule                                                |
| Type           | String                                                  |
| Valeur par défaut        | N/A                                                     |
| Système minimal | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si les événements sont suivis. Les événements incluent des actions telles que l’arrêt de l’application ; création et publication d’objets ; références d’objet, cohérence, activation et désactivation ; appels de méthode, retours et exceptions ; démarrage de la transaction, préparation à la validation et abandon ; connexion, allocation et recyclage des distributions de ressources ; allocation et recyclage des threads. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                     |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Default        | Vrai                                                                                                                                                                                                                                                                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>ExceptionClass



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | CLSID, qui peut être un GUID ou une chaîne de moniker, pour activer un autre programme pendant le processus de traitement d’un programme de composants en file d’attente qui échoue à plusieurs reprises. |
| Access         | Lecture/écriture                                                                                                                                                                 |
| Type           | String                                                                                                                                                                    |
| Valeur par défaut        | ""                                                                                                                                                                        |
| Système minimal | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------|
| Description    | Active les événements à déclencher en parallèle si le composant est une classe d’événements. |
| Access         | Lecture/écriture                                                                  |
| Type           | Bool                                                                       |
| Default        | False                                                                      |
| Système minimal | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Permet de passer des propriétés de contexte IIS, telles qu’un objet de session d’application ou un objet de session utilisateur, dans le contexte de cette classe. |
| Access         | Lecture/écriture                                                                                                                                   |
| Type           | Bool                                                                                                                                        |
| Default        | False                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------|
| Description    | Indique si le composant est utilisé pour initialiser une application serveur. |
| Access         | Lecture/écriture                                                                   |
| Type           | Bool                                                                        |
| Default        | False                                                                       |
| Système minimal | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Description    | False si l’application ou le composant COM+ est désactivé. Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true. |
| Access         | Lecture/écriture                                                                                                                   |
| Type           | Bool                                                                                                                        |
| Default        | Vrai                                                                                                                        |
| Système minimal | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| Entrée | Valeur |
|----------------|----------------------------------------------------|
| Description    | Indique si le composant est une classe d’événements. |
| Access         | Lecture seule                                           |
| Type           | Bool                                               |
| Default        | False                                              |
| Système minimal | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------|
| Description    | Indique si le composant est installé dans une application. |
| Access         | Lecture seule                                                        |
| Type           | Bool                                                            |
| Default        | False                                                           |
| Système minimal | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si une application serveur est un composant privé. Un composant privé dans une application serveur ne peut être activé qu’à partir de l’application. Par exemple, si vous appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) sur un composant privé, il échoue à partir de out-of-process mais fonctionne en mode in-process. En revanche, si vous appelez **CoCreateInstance** sur un composant public, il est exécuté en mode in-process et out-of-process. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Default        | False                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si l' [activation JIT](enabling-jit-activation-for-a-component.md) est activée pour le composant. Cette propriété a la valeur true lorsque la [prise en charge des transactions](setting-the-transaction-attribute.md) est définie sur obligatoire, nécessite une nouvelle ou est prise en charge. Lorsque JustInTimeActivation est défini sur true, la [prise en charge](setting-the-synchronization-attribute.md) de la synchronisation doit être définie sur Required (valeur par défaut) ou nécessite New. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Default        | False                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Si le service d’équilibrage de charge des composants est installé et activé sur le serveur, détermine si le composant participe à l’équilibrage de charge. |
| Access         | Lecture/écriture                                                                                                                                        |
| Type           | Bool                                                                                                                                             |
| Default        | False                                                                                                                                            |
| Système minimal | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Entrée | Valeur |
|----------------|-----------------------------------|
| Description    | Nombre maximal d’objets regroupés. |
| Access         | Lecture/écriture                         |
| Type           | Long (1-1048576)                  |
| Default        | 1 048 576                           |
| Système minimal | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Entrée | Valeur |
|----------------|-----------------------------------|
| Description    | Nombre minimal d’objets regroupés. |
| Access         | Lecture/écriture                         |
| Type           | Long (0-1048576)                  |
| Default        | 0                                 |
| Système minimal | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------|
| Description    | CLSID du filtre de l’éditeur utilisé si le composant est une classe d’événements. |
| Access         | Lecture/écriture                                                               |
| Type           | String                                                                  |
| Valeur par défaut        | N/A                                                                     |
| Système minimal | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientContext



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------|
| Description    | Indique que le composant doit être activé dans le contexte de son appelant d’origine. Dans le cas contraire, l’activation échoue. |
| Access         | Lecture/écriture                                                                                                 |
| Type           | Bool                                                                                                      |
| Default        | False                                                                                                     |
| Système minimal | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultContext



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------|
| Description    | Indique que le composant doit être activé dans le contexte de l’appelant par défaut. Dans le cas contraire, l’activation échoue. |
| Access         | Lecture/écriture                                                                                                    |
| Type           | Bool                                                                                                         |
| Default        | False                                                                                                        |
| Système minimal | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------|
| Description    | Détermine si le [regroupement d’objets com+](com--object-pooling.md) est activé pour le composant. |
| Access         | Lecture/écriture                                                                                       |
| Type           | Bool                                                                                            |
| Default        | False                                                                                           |
| Système minimal | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom convivial utilisé pour identifier le composant. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                |
| Valeur par défaut        | N/A                                                                                                                                                                                   |
| Système minimal | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------|
| Description    | Identificateur de l’éditeur d’événements si le composant est une classe d’événements. |
| Access         | Lecture/écriture                                                              |
| Type           | String                                                                 |
| Valeur par défaut        | ""                                                                     |
| Système minimal | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------|
| Description    | GUID identifiant l’assembly du GAC qui est exécuté lorsque le composant est appelé en tant que service SOAP. |
| Access         | Lecture/écriture                                                                                        |
| Type           | String                                                                                           |
| Valeur par défaut        | NULL                                                                                             |
| Système minimal | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------|
| Description    | Nom du type managé pour un composant qui peut être appelé en tant que service SOAP. |
| Access         | Lecture/écriture                                                                    |
| Type           | String                                                                       |
| Valeur par défaut        | NULL                                                                         |
| Système minimal | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Synchronisation



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine la [synchronisation](setting-the-synchronization-attribute.md) des appels pour le composant.                                                                                                     |
| Access         | Lecture/écriture                                                                                                                                                                                           |
| Type           | Valeurs possibles longues : COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4) |
| Default        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                  |
| Système minimal | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine le mode d’affectation des instances du composant aux threads pour l’exécution de la méthode. Les valeurs correspondent aux modèles de thread COM.                                                                                        |
| Access         | Lecture seule                                                                                                                                                                                                                  |
| Type           | Valeurs possibles longues : COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5) |
| Default        | N/A                                                                                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transaction



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine la façon dont un composant prend en charge les [transactions](setting-the-transaction-attribute.md). Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques. |
| Access         | Lecture/écriture                                                                                                                                                                              |
| Type           | Valeurs possibles longues : COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)        |
| Default        | COMAdminTransactionNone (1)                                                                                                                                                            |
| Système minimal | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>TxIsolationLevel



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique les niveaux d’isolation de la transaction. Il existe cinq niveaux d’isolement : aucun, lecture non validée, lecture validée, lecture renouvelable et sérialisé. Le niveau d’isolation par défaut est sérialisé.                           |
| Access         | Lecture/écriture                                                                                                                                                                                                                  |
| Type           | Valeurs possibles longues : COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4) |
| Default        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                   |
| Système minimal | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Entrée | Valeur |
|----------------|---------------------------|
| Description    | Identificateur de la build de la version. |
| Access         | Lecture seule                  |
| Type           | String                    |
| Valeur par défaut        | ""                        |
| Système minimal | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Entrée | Valeur |
|----------------|---------------------|
| Description    | Identificateur de version. |
| Access         | Lecture seule            |
| Type           | String              |
| Valeur par défaut        | ""                  |
| Système minimal | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Entrée | Valeur |
|----------------|-------------------------|
| Description    | Sous-identificateur de version. |
| Access         | Lecture seule                |
| Type           | String                  |
| Valeur par défaut        | ""                      |
| Système minimal | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| Entrée | Valeur |
|----------------|-------------------------------|
| Description    | Identificateur de sous-Build de version. |
| Access         | Lecture seule                      |
| Type           | String                        |
| Valeur par défaut        | ""                            |
| Système minimal | Windows 2000                  |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
