---
description: Contient un objet pour chaque application COM+ installée sur l’ordinateur local. Les propriétés exposées par ces objets conservent tous les paramètres effectués au niveau de l’application.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Collection d’applications
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 23ce8d7dc343e9cbca9aab642aee99424c5fffdde8ef0f15a52d2959bf492095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549423"
---
# <a name="applications-collection"></a>Collection d’applications

Contient un objet pour chaque application COM+ installée sur l’ordinateur local. Les propriétés exposées par ces objets conservent tous les paramètres effectués au niveau de l’application.

Vous définissez les propriétés des composants dans une application à l’aide de la collection de [**composants**](components.md) associés. Vous attribuez des rôles à une application à l’aide de la collection de [**rôles**](roles.md) associée.

Pour installer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) . Pour installer une application à partir d’un fichier ou pour arrêter ou exporter une application, utilisez également des méthodes sur l’objet **COMAdminCatalog** . Sinon, pour créer une nouvelle application, vous pouvez ajouter un objet à la collection d' **applications** .

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection d' **applications** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Composants**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Rôles**](roles.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Partitions**](partitions.md)
-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Activation](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [Authentification](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Modifiable](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Supprimé](#deleteable)
-   [Description](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [Identifiant](#applications-collection)
-   [Identité](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Nom](#applicationproxyservername)
-   [Mot de passe](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replicable](#replicable)
-   [RunForever](#runforever)
-   [FormName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique si l’application peut utiliser 3 Go de mémoire dans son processus. Si cette option n’est pas activée, l’application ne peut utiliser que 2 Go de mémoire. |
| Accès         | Lecture/écriture                                                                                                                                     |
| Type           | Bool                                                                                                                                          |
| Default        | False                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique si les contrôles d’accès sont effectués uniquement au niveau du processus ou au niveau du processus et du composant. Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques. |
| Accès         | Lecture/écriture                                                                                                                                                                                                       |
| Type           | Longues valeurs possibles : COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Default        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Système minimal | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Activation



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | L’activation locale indique que les objets de l’application s’exécutent dans un processus serveur local dédié (application serveur). L’activation en cours indique que les objets s’exécutent dans le processus de leur créateur (application de bibliothèque). |
| Accès         | Lecture/écriture                                                                                                                                                                                                                           |
| Type           | Longues valeurs possibles : COMAdminActivationInproc (0) COMAdminActivationLocal (1)                                                                                                                                                        |
| Default        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------|
| Description    | Indique si les contrôles d’accès sont effectués pour l’application lorsque les clients y effectuent des appels. |
| Accès         | Lecture/écriture                                                                                          |
| Type           | Bool                                                                                               |
| Default        | True                                                                                               |
| Système minimal | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Chemin d’accès complet à l’application. Ces informations sont nécessaires lorsque vous configurez des assemblys côte à côte (SxS). les assemblys côte à côte (SxS) permettent aux applications ASP de spécifier la version d’une DLL système prise en charge par SxS à utiliser, telle que MSVCRT, MSXML, COMCTL, GDIPLUS, etc. Par exemple, si votre application ASP repose sur la version 2,0 de MSVCRT, vous pouvez vous assurer que votre application utilise toujours la version 2,0 de MSVCRT même après l’application des service packs au serveur. Toute nouvelle version de MSVCRT est toujours installée sur l’ordinateur, mais la version 2,0 reste et est utilisée par votre application. Les dll prises en charge par SxS sont stockées dans% WINDIR% \\ WinSxS. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Valeur par défaut        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Une seule version d’une DLL système peut être utilisée dans n’importe quel pool d’applications, même si cette fonctionnalité est configurable au niveau de l’application. Par exemple, si l’application App1 utilise MSVCRT, version 2,5 et que l’application App2 utilise MSVCRT, version 2,4, App1 et App2 ne doivent pas figurer dans le même pool d’applications. Si c’est le cas, l’application qui est chargée en premier a sa version de MSVCRT chargée, et l’autre application est obligée de l’utiliser jusqu’à ce que les applications soient déchargées.

 

Pour plus d’informations, consultez « assemblys côte à côte » dans [modifications dans les services com+ dans IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).

### <a name="applicationproxy"></a>ApplicationProxy



| Entrée | Valeur |
|----------------|------------------------------------------------------------|
| Description    | Indique si l’application est un proxy d’application. |
| Accès         | Lecture seule                                                   |
| Type           | Bool                                                       |
| Default        | False                                                      |
| Système minimal | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de serveur distant utilisé lors de l’exportation du proxy d’application. Il s’agit du nom du serveur vers lequel pointe le proxy d’application lorsqu’il est installé sur un ordinateur client. |
| Accès         | Lecture/écriture                                                                                                                                                              |
| Type           | String                                                                                                                                                                 |
| Valeur par défaut        | ""                                                                                                                                                                     |
| Système minimal | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Entrée | Valeur |
|----------------|---------------------------------------------------|
| Description    | GUID représentant l’ID de la partition d’application. |
| Accès         | Lecture seule                                          |
| Type           | String                                            |
| Valeur par défaut        | <Generated>                                 |
| Système minimal | Windows Server 2003                               |



 

### <a name="authentication"></a>Authentification



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit le niveau d’authentification pour les appels, avec les valeurs correspondant aux paramètres d’authentification de l’appel de procédure distante (RPC). Lorsque COMAdminAuthenticationDefault est choisi, le paramètre dans la propriété DefaultAuthenticationLevel de la collection [**LocalComputer**](localcomputer.md) est utilisé. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                             |
| Type           | Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Default        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Pour les applications de bibliothèque (in-process), les seuls paramètres valides sont COMAdminAuthenticationDefault et COMAdminAuthenticationNone. Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine l’identité qui est présentée lorsque les appels sont empruntés.                                                                                                                                                                      |
| Accès         | Lecture/écriture                                                                                                                                                                                                                               |
| Type           | Valeurs possibles longues : COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0X2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Default        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Modifiable



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si les modifications apportées aux paramètres d’application ou à ceux de ses composants sont autorisées, par programmation ou par le biais de l’outil d’administration Services de composants. |
| Accès         | Lecture/écriture                                                                                                                                                                     |
| Type           | Bool                                                                                                                                                                          |
| Default        | True                                                                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne de ligne de commande à utiliser lors du débogage. L’application peut être lancée dans un débogueur avec la ligne de commande spécifiée. |
| Accès         | Lecture/écriture                                                                                                                  |
| Type           | String                                                                                                                     |
| Valeur par défaut        | ""                                                                                                                         |
| Système minimal | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------|
| Description    | Spécifie le nombre maximal d’applications regroupables pouvant s’exécuter simultanément. |
| Accès         | Lecture/écriture                                                                        |
| Type           | Long (1-1048576)                                                                 |
| Default        | 1                                                                                |
| Système minimal | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Entrée | Valeur |
|----------------|---------------------------------------------------------------|
| Description    | Chaîne informatif pour décrire qui a créé l’application. |
| Accès         | Lecture/écriture                                                     |
| Type           | String                                                        |
| Valeur par défaut        | ""                                                            |
| Système minimal | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Entrée | Valeur |
|----------------|------------------------------------------------------------------|
| Description    | Détermine si le Gestionnaire des ressources de compensation est activé. |
| Accès         | Lecture/écriture                                                        |
| Type           | Bool                                                             |
| Default        | False                                                            |
| Système minimal | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| Description    | Nom et chemin d’accès du fichier pour conserver le journal pour le CRM (Compensating Resource Manager). |
| Accès         | Lecture/écriture                                                                              |
| Type           | String                                                                                 |
| Valeur par défaut        | ""                                                                                     |
| Système minimal | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Supprimé



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit si l’application peut être supprimée, soit par programme, soit par le biais de l’outil d’administration Services de composants. |
| Accès         | Lecture/écriture                                                                                                                   |
| Type           | Bool                                                                                                                        |
| Default        | True                                                                                                                        |
| Système minimal | Windows 2000                                                                                                                |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|----------------------------|
| Description    | Décrit l’application. |
| Accès         | Lecture/écriture                  |
| Type           | String                     |
| Valeur par défaut        | ""                         |
| Système minimal | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------|
| Description    | Active le vidage de l’état d’une application COM+ au moment de l’échec dans un répertoire désigné. |
| Accès         | Lecture/écriture                                                                                             |
| Type           | Bool                                                                                                  |
| Default        | False                                                                                                 |
| Système minimal | Windows XP                                                                                            |



 

> [!Note]  
> À partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux fichiers de vidage COM+.

 

### <a name="dumponexception"></a>DumpOnException



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Active le vidage de l’état d’une application COM+ lorsque l’application provoque une exception non gérée et se termine par le runtime COM+. |
| Accès         | Lecture/écriture                                                                                                                                     |
| Type           | Bool                                                                                                                                          |
| Default        | False                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------|
| Description    | Active le vidage de l’état d’une application COM+ en cas d’échec de l’application. |
| Accès         | Lecture/écriture                                                                       |
| Type           | Bool                                                                            |
| Default        | False                                                                           |
| Système minimal | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Entrée | Valeur |
|----------------|--------------------------------------------------------------|
| Description    | Chemin d’accès du répertoire dans lequel les fichiers de vidage sont enregistrés. |
| Accès         | Lecture/écriture                                                    |
| Type           | String                                                       |
| Valeur par défaut        | « % systemroot% \\ system32 \\ com \\ DMP »                           |
| Système minimal | Windows XP                                                   |



 

> [!Note]  
> À partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux fichiers de vidage COM+.

 

### <a name="eventsenabled"></a>EventsEnabled



| Entrée | Valeur |
|----------------|-----------------------------------------------------------|
| Description    | Indique si les événements sont activés pour l’application. |
| Accès         | Lecture/écriture                                                 |
| Type           | Bool                                                      |
| Default        | True                                                      |
| Système minimal | Windows 2000                                              |



 

### <a name="id"></a>ID



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID représentant l’application. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                            |
| Type           | String                                                                                                                                                               |
| Valeur par défaut        | <Generated>                                                                                                                                                    |
| Système minimal | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identité



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit l’identité du processus serveur pour l’application. Spécifiez un compte d’utilisateur valide ou un « utilisateur interactif » pour que l’application assume l’identité de l’utilisateur actuellement connecté. Vous pouvez également spécifier les chaînes « NT Authority \\ LocalService », « NT Authority \\ NetworkService » et « NT Authority \\ System ». Le mot de passe par défaut de ces trois comptes est «» (chaîne vide). |
| Accès         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Default        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

La propriété Identity n’est pas activée pour les applications de bibliothèque, qui s’exécutent dans le processus client.

La propriété de mot de passe doit être définie en même temps que l’identité, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés. Si le mot de passe et l’identité ne sont pas synchronisés, l’application ne peut pas être lancée tant qu’elle n’est pas réinitialisée par un administrateur.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit le niveau d’emprunt d’identité utilisé pour les appels effectués à d’autres applications.                                                                                           |
| Accès         | Lecture/écriture                                                                                                                                                     |
| Type           | Valeurs possibles longues : COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Default        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Si l’application ou le composant COM+ est désactivé, IsEnabled a la valeur false. Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true. |
| Accès         | Lecture/écriture                                                                                                                                 |
| Type           | Bool                                                                                                                                      |
| Default        | True                                                                                                                                      |
| Système minimal | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Entrée | Valeur |
|----------------|--------------------------------------|
| Description    | Identifie les applications système COM+. |
| Accès         | Lecture seule                             |
| Type           | Bool                                 |
| Default        | False                                |
| Système minimal | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------|
| Description    | Indique le nombre maximal de fichiers à générer avant le remplacement. |
| Accès         | Lecture/écriture                                                                        |
| Type           | Long (1-200)                                                                     |
| Default        | 5                                                                                |
| Système minimal | Windows XP                                                                       |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Le nom de l’application. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                               |
| Valeur par défaut        | « Nouvelle application »                                                                                                                                                                                                                    |
| Système minimal | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Vous devez choisir des noms uniques pour les applications. Si plusieurs applications sont créées avec le même nom, elle peut interférer avec le référencement des applications par nom, ce qui entraîne un comportement imprévisible.

 

### <a name="password"></a>Mot de passe



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------|
| Description    | Définit le mot de passe utilisé par le processus serveur pour se connecter sous l’identité. |
| Accès         | WriteOnly                                                                  |
| Type           | String                                                                     |
| Valeur par défaut        | ""                                                                         |
| Système minimal | Windows 2000                                                               |



 

Le mot de passe doit être défini en même temps que l’identité, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés. Si le mot de passe et l’identité ne sont pas synchronisés, l’application ne peut pas être lancée tant qu’elle n’est pas réinitialisée par un administrateur.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique dans quelles circonstances les demandes mises en file d’attente vers une application sont authentifiées.                                                 |
| Accès         | Lecture/écriture                                                                                                                               |
| Type           | Longues valeurs possibles : COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2) |
| Default        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Système minimal | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le nombre maximal de threads d’écoute simultanés. La plage valide pour cette propriété est comprise entre 0 et 1000. Pour une application nouvellement créée, le paramètre est dérivé de l’algorithme actuellement utilisé pour déterminer le nombre par défaut de threads de l’écouteur : 16 fois le nombre de processeurs dans le serveur. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                 |
| Type           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Default        | 0                                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Cette propriété est également disponible avec la fonctionnalité de lecture/écriture à partir de l’onglet mise en **file d’attente** de l’outil d’administration Services de composants.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique si l’écouteur de composants en file d’attente est activé pour l’application. S’il est activé, l’écouteur est lancé au démarrage de l’application. Cette propriété prend effet uniquement si QueuingEnabled a la valeur true. |
| Accès         | Lecture/écriture                                                                                                                                                                                                            |
| Type           | Bool                                                                                                                                                                                                                 |
| Default        | False                                                                                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| Description    | Indique si le service de composants en file d’attente COM+ est activé pour l’application. |
| Accès         | Lecture/écriture                                                                            |
| Type           | Bool                                                                                 |
| Default        | False                                                                                |
| Système minimal | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le nombre maximal d’activations d’objets configurés dans l’application à accepter avant de recycler le processus. Le nombre d’activations par défaut est 0. |
| Accès         | Lecture/écriture                                                                                                                                                            |
| Type           | Long (0-1048576)                                                                                                                                                     |
| Default        | 0                                                                                                                                                                    |
| Système minimal | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le nombre maximal d’appels pour autoriser les objets configurés dans l’application à accepter avant de recycler le processus. Le nombre d’appels par défaut est 0. |
| Accès         | Lecture/écriture                                                                                                                                                      |
| Type           | Long (0-1048576)                                                                                                                                               |
| Default        | 0                                                                                                                                                              |
| Système minimal | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique la durée (en minutes) nécessaire à l’exécution d’un processus recyclé avant son arrêt. Le compte à rebours commence immédiatement après le recyclage du processus. Le délai d’expiration maximal est de 1440 minutes (24 heures) et la valeur par défaut est 15 minutes. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                        |
| Type           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Default        | 15                                                                                                                                                                                                                                                               |
| Système minimal | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le nombre maximal de minutes pendant lesquelles un processus doit être exécuté avant de le recycler. La limite de durée de vie maximale est de 30240 minutes (21 jours) et la valeur par défaut est 0 minute. |
| Accès         | Lecture/écriture                                                                                                                                                                   |
| Type           | Long (0-30240)                                                                                                                                                              |
| Default        | 0                                                                                                                                                                           |
| Système minimal | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique la quantité maximale d’utilisation de la mémoire (en kilo-octets) autorisée pour un processus avant son recyclage. Si l’utilisation de la mémoire de processus dépasse le nombre spécifié pendant une période supérieure à une minute, le processus est recyclé. La quantité d’utilisation de la mémoire par défaut est de 0 Ko. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                              |
| Type           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Default        | 0                                                                                                                                                                                                                                                                      |
| Système minimal | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replicable



| Entrée | Valeur |
|----------------|------------------------------------------------------|
| Description    | Indique si l’application peut être répliquée. |
| Accès         | Lecture/écriture                                            |
| Type           | Bool                                                 |
| Default        | True                                                 |
| Système minimal | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Permet à un processus serveur de continuer si une application est inactive. Si la valeur est true, le processus serveur ne s’arrête pas quand il est resté inactif. Si la valeur est false, le processus s’arrête en fonction de la valeur définie par la propriété ShutdownAfter. RunForever n’est pas activé pour les applications de bibliothèque (in-process). |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                |
| Type           | Bool                                                                                                                                                                                                                                                                                                     |
| Default        | False                                                                                                                                                                                                                                                                                                    |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>NomService



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du service correspondant à l’application configurée pour s’exécuter en tant qu’application de service. Si cette valeur est **null**, l’application n’est pas configurée pour s’exécuter en tant que service. Dans le cas contraire, les informations de configuration du service sont disponibles à l’aide du nom du service. |
| Accès         | Lecture seule                                                                                                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                                                                                                           |
| Valeur par défaut        | ""                                                                                                                                                                                                                                                                               |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit le délai avant l’arrêt d’un processus serveur lorsqu’il devient inactif. La latence d’arrêt est comprise entre 0 et 1440 minutes (24 heures). Si RunForever a la valeur true, cette propriété est ignorée. ShutdownAfter n’est pas activé pour les applications de bibliothèque (in-process). |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                          |
| Type           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Default        | 3                                                                                                                                                                                                                                                                  |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| Description    | Indique si cette application est exposée pour être consommée via le protocole SOAP. |
| Accès         | Lecture/écriture                                                                            |
| Type           | Bool                                                                                 |
| Default        | False                                                                                |
| Système minimal | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------|
| Description    | Point de terminaison d’URL auquel cette application est exposée via le protocole SOAP. |
| Accès         | Lecture/écriture                                                                    |
| Type           | String                                                                       |
| Valeur par défaut        | ""                                                                           |
| Système minimal | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------|
| Description    | Adresse de messagerie à laquelle cette application est exposée par le biais du protocole SOAP. |
| Accès         | Lecture/écriture                                                                     |
| Type           | String                                                                        |
| Valeur par défaut        | ""                                                                            |
| Système minimal | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Description    | Répertoire racine virtuel IIS dans lequel les scripts d’accès qui exposent l’application via le protocole SOAP résident. |
| Accès         | Lecture/écriture                                                                                                            |
| Type           | String                                                                                                               |
| Valeur par défaut        | ""                                                                                                                   |
| Système minimal | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine la stratégie de restriction logicielle (SRP) pour l’application. Si la valeur est true, la propriété SRPTrustLevel de l’application est utilisée. Si la valeur est false, les stratégies de restriction logicielle des paramètres de sécurité locaux sont utilisées. Les paramètres de sécurité locaux sont contrôlés par le biais du composant logiciel enfichable Stratégie de sécurité locale de la console MMC (Microsoft Management Console). |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                             |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Default        | False                                                                                                                                                                                                                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le niveau de confiance de la stratégie de restriction logicielle (SRP) de l’application. Cette propriété est utilisée uniquement si la propriété SRPEnabled a la valeur true. Le niveau de confiance du SRP fait référence au niveau de confiance que vous êtes prêt à accorder à une application. Un niveau de confiance SRP non restreint correspond à la \_ valeur enum LEVELID FULLYTRUSTED plus sécurisée \_ , tandis qu’un niveau de confiance SRP non autorisé correspond à la \_ valeur enum non autorisée LEVELID plus sûre \_ . L’énumération pour les niveaux de confiance est définie dans Winsafer. h. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Type           | Valeurs possibles longues : LEVELID sécurisé \_ non \_ autorisé (0x0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Default        | SÉCURITÉ \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Une application que vous êtes disposé à approuver avec un accès non restreint doit avoir la sécurité la plus stricte qui lui est attachée. Les applications non restreintes ne peuvent charger que des composants non restreints, tandis que les applications non autorisées ne sont pas autorisées à s’exécuter et ne peuvent donc pas charger de composants.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
