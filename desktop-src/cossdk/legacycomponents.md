---
description: Contient un objet pour chaque composant non configuré dans la collection d’applications. Les composants non configurés ne peuvent pas utiliser les services COM+. Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Collection LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311010"
---
# <a name="legacycomponents-collection"></a>Collection LegacyComponents

Contient un objet pour chaque composant non configuré dans la collection d’applications. Les composants non configurés ne peuvent pas utiliser les services COM+. Les propriétés exposées par ces objets contiennent les paramètres effectués au niveau du composant.

Cette collection prend en charge la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mais pas la méthode [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Pour installer ou importer des composants dans une application, utilisez des méthodes sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membres

La collection **LegacyComponents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Applications**](applications.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Nombre de bits](#bitness)
-   [NomClasse](#classname)
-   [IDENTIFICATEUR](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [Mot de passe](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [ServiceParameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------|
| Description    | Spécifie les comptes d’utilisateurs qui sont autorisés ou non à accéder au composant. |
| Access         | Lecture/écriture                                                                       |
| Type           | String                                                                          |
| Valeur par défaut        | N/A                                                                             |
| Système minimal | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Entrée | Valeur |
|----------------|------------------------------------------------------------------|
| Description    | Spécifie si le serveur doit être exécuté sur l’ordinateur de stockage de données. |
| Access         | Lecture/écriture                                                        |
| Type           | Valeurs possibles de chaîne : "N" "Y"                                    |
| Default        | "N"                                                              |
| Système minimal | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Entrée | Valeur |
|----------------|---------------------|
| Description    | L’ID de l'application. |
| Access         | Lecture seule            |
| Type           | String              |
| Valeur par défaut        | N/A                 |
| Système minimal | Windows XP          |



 

### <a name="appname"></a>AppName



| Entrée | Valeur |
|----------------|------------------------------|
| Description    | Le nom de l’application. |
| Access         | Lecture seule                     |
| Type           | String                       |
| Valeur par défaut        | N/A                          |
| Système minimal | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit le niveau d’authentification pour les appels, avec les valeurs correspondant aux paramètres d’authentification de l’appel de procédure distante (RPC). Lorsque COMAdminAuthenticationDefault est choisi, le paramètre dans la propriété DefaultAuthenticationLevel de la collection [**LocalComputer**](localcomputer.md) est utilisé. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                             |
| Type           | Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Default        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.

 

### <a name="bitness"></a>Nombre de bits



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Représente le type de bits binaire du composant. sur les systèmes qui utilisent la Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits. |
| Access         | Lecture seule                                                                                                                                                              |
| Type           | Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                         |
| Default        | N/A                                                                                                                                                                   |
| Système minimal | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Entrée | Valeur |
|----------------|------------------------|
| Description    | Nom de la classe. |
| Access         | Lecture seule               |
| Type           | String                 |
| Valeur par défaut        | N/A                    |
| Système minimal | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID du composant. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Valeur par défaut        | N/A                                                                                                                                                       |
| Système minimal | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Entrée | Valeur |
|----------------|------------------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à une application serveur surragate. |
| Access         | Lecture/écriture                                                  |
| Type           | String                                                     |
| Valeur par défaut        | N/A                                                        |
| Système minimal | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à une DLL du gestionnaire personnalisé in-process 32 bits. |
| Access         | Lecture/écriture                                                          |
| Type           | String                                                             |
| Valeur par défaut        | N/A                                                                |
| Système minimal | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrée | Valeur |
|----------------|------------------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à une DLL de serveur in-process 32 bits. |
| Access         | Lecture/écriture                                                  |
| Type           | String                                                     |
| Valeur par défaut        | N/A                                                        |
| Système minimal | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Si l’application ou le composant COM+ est désactivé, IsEnabled a la valeur false. Si l’application ou le composant COM+ est activé, IsEnabled a la valeur true. |
| Access         | Lecture/écriture                                                                                                                                 |
| Type           | Bool                                                                                                                                      |
| Default        | Vrai                                                                                                                                      |
| Système minimal | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| Description    | Spécifie les comptes d’utilisateurs autorisés ou non à démarrer ce composant. |
| Access         | Lecture/écriture                                                                              |
| Type           | String                                                                                 |
| Valeur par défaut        | N/A                                                                                    |
| Système minimal | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à une application serveur locale 32 bits. Pour aider à protéger la sécurité du système, utilisez des chaînes entre guillemets dans le chemin d’accès pour indiquer l’emplacement où se termine le nom de fichier exécutable et les arguments Begin. Par exemple, « \\ C : \\ Program Files fichiers de la \\ société \\Application.exe\\ «param1 param2 ». |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                                                      |
| Valeur par défaut        | N/A                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| Entrée | Valeur |
|----------------|-----------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à l’application de service. |
| Access         | Lecture/écriture                                           |
| Type           | String                                              |
| Valeur par défaut        | N/A                                                 |
| Système minimal | Windows XP                                          |



 

### <a name="password"></a>Mot de passe



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Définit le mot de passe utilisé par le processus serveur pour ouvrir une session sous l’identité RunAs spécifiée. Le mot de passe doit être défini en même temps que l’identité RunAs, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés. Si le mot de passe et l’identité ne sont pas synchronisés, le composant ne peut pas être lancé tant qu’il n’est pas réinitialisé par un administrateur. |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Valeur par défaut        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom identifiant le composant. Cette propriété est retournée lorsque la méthode de propriété Name est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                             |
| Type           | String                                                                                                                               |
| Valeur par défaut        | N/A                                                                                                                                  |
| Système minimal | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Entrée | Valeur |
|----------------|---------------------------------------|
| Description    | Spécifie l’ordinateur serveur distant. |
| Access         | Lecture/écriture                             |
| Type           | String                                |
| Valeur par défaut        | N/A                                   |
| Système minimal | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Spécifie l’utilisateur sous dont l’identité doit être exécutée par le composant. Le mot de passe doit être défini en même temps que l’identité RunAs, avant d’utiliser [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), car le mot de passe et l’identité sont validés avant d’être enregistrés. Si le mot de passe et l’identité ne sont pas synchronisés, le composant ne peut pas être lancé tant qu’il n’est pas réinitialisé par un administrateur. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Valeur par défaut        | N/A                                                                                                                                                                                                                                                                                                                                                                                               |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------|
| Description    | Spécifie les paramètres passés à l’application lorsqu’elle est appelée en tant qu’application de service. |
| Access         | Lecture/écriture                                                                                 |
| Type           | String                                                                                    |
| Valeur par défaut        | N/A                                                                                       |
| Système minimal | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique le niveau de confiance de la stratégie de restriction logicielle (SRP) du composant. Le niveau de confiance du SRP fait référence au niveau de confiance que vous êtes prêt à attribuer à un composant. Un niveau de confiance SRP non restreint correspond à la \_ valeur enum LEVELID FULLYTRUSTED plus sécurisée \_ , tandis qu’un niveau de confiance SRP non autorisé correspond à la \_ valeur enum non autorisée LEVELID plus sûre \_ . L’énumération pour les niveaux de confiance est définie dans Winsafer. h. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Type           | Valeurs possibles longues : LEVELID sécurisé \_ non \_ autorisé (0x0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Default        | \_FULLYTRUSTED LEVELID plus \_ sécurisé                                                                                                                                                                                                                                                                                                                                                                                                        |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La sécurité la plus stricte doit être attachée à un composant que vous êtes disposé à approuver avec un accès non restreint. Les applications non restreintes ne peuvent charger que des composants non restreints, tandis que les applications non autorisées ne sont pas autorisées à s’exécuter et ne peuvent donc pas charger de composants.

### <a name="threadingmodel"></a>ThreadingModel



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine le mode d’affectation des instances du composant aux threads pour l’exécution de la méthode. Les valeurs correspondent aux modèles de thread COM.                                                  |
| Access         | Lecture seule                                                                                                                                                                            |
| Type           | Valeurs possibles longues : COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) |
| Default        | N/A                                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
