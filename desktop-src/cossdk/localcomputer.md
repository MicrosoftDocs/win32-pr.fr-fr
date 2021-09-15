---
description: Contient un objet unique qui correspond à l’ordinateur dont vous accédez au catalogue. Cet objet contient des informations sur les paramètres au niveau de l’ordinateur.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Collection LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311001"
---
# <a name="localcomputer-collection"></a>Collection LocalComputer

Contient un objet unique qui correspond à l’ordinateur dont vous accédez au catalogue. Cet objet contient des informations sur les paramètres au niveau de l’ordinateur. si vous appelez la méthode [**Connecter**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) sur un objet créé à partir de la classe [**COMAdminCatalog**](comadmincatalog.md) , l’objet de la collection **LocalComputer** contient des informations sur l’ordinateur distant dont vous accédez au catalogue.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **LocalComputer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Description](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [IsRouter](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [Nom](#name)
-   [OperatingSystem](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [Ports](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| Entrée | Valeur |
|----------------|------------------------------------------------------------|
| Description    | Nom du serveur distant utilisé par les proxys d’application par défaut. |
| Access         | Lecture/écriture                                                  |
| Type           | String                                                     |
| Valeur par défaut        | ""                                                         |
| Système minimal | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Entrée | Valeur |
|----------------|-----------------------------------------------------|
| Description    | Indique si les services Internet COM sont activés. |
| Access         | Lecture/écriture                                           |
| Type           | Bool                                                |
| Default        | False                                               |
| Système minimal | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Entrée | Valeur |
|----------------|---------------------------------------------|
| Description    | Affectez la valeur true pour activer DCOM sur l’ordinateur. |
| Access         | Lecture/écriture                                   |
| Type           | Bool                                        |
| Default        | Vrai                                        |
| Système minimal | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Niveau d’authentification utilisé par les applications dont l’authentification est définie sur par défaut. Les valeurs correspondent aux paramètres d’authentification de l’appel de procédure distante (RPC).                                                                                         |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                |
| Type           | Valeurs possibles longues : COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) |
| Default        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Système minimal | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault est mappé à COMAdminAuthenticationConnect quand COM appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Il est recommandé d’utiliser les constantes dans l’énumération et non les valeurs numériques.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Niveau d’emprunt d’identité à autoriser si aucun n’est défini.                                                                                                               |
| Access         | Lecture/écriture                                                                                                                                                     |
| Type           | Valeurs possibles longues : COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Default        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Système minimal | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Il est recommandé d’utiliser les constantes dans l’énumération, et non les valeurs numériques.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------|
| Description    | Détermine si le type de port par défaut fourni doit être Internet (true) ou intranet (false). |
| Access         | Lecture/écriture                                                                                           |
| Type           | Bool                                                                                                |
| Default        | False                                                                                               |
| Système minimal | Windows 2000                                                                                        |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|--------------------------------|
| Description    | Description de l’ordinateur. |
| Access         | Lecture/écriture                      |
| Type           | String                         |
| Valeur par défaut        | ""                             |
| Système minimal | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| Description    | Indique si l’utilisateur des mappages de partition est archivé dans le magasin de domaines. |
| Access         | Lecture/écriture                                                                              |
| Type           | Bool                                                                                   |
| Default        | Vrai                                                                                   |
| Système minimal | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine si les ports répertoriés dans la propriété ports doivent être utilisés pour Internet (true) ou pour l’intranet (false). |
| Access         | Lecture/écriture                                                                                                             |
| Type           | Bool                                                                                                                  |
| Default        | False                                                                                                                 |
| Système minimal | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Affectez la valeur true si l’ordinateur est un routeur pour le service d’équilibrage de charge des composants (CLB). Cette propriété ne peut être définie sur true que si le service d’équilibrage de charge de composant est actuellement installé sur l’ordinateur. Sinon, les erreurs avec comadmin \_ E \_ requièrent une \_ \_ plateforme différente. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                           |
| Type           | Bool                                                                                                                                                                                                                                                                                |
| Default        | False                                                                                                                                                                                                                                                                               |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                        |



 

Si cette propriété est définie sur true, le serveur CLB est configuré et démarre au démarrage. Le serveur est ajouté à la collection ApplicationCluster si elle n’est pas déjà présente.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Entrée | Valeur |
|----------------|-------------------------------------|
| Description    | CLSID de l’objet à équilibrer. |
| Access         | Lecture/écriture                           |
| Type           | String                              |
| Valeur par défaut        | NULL                                |
| Système minimal | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| Description    | Indique si l’utilisateur des mappages de partition est archivé dans le magasin local. |
| Access         | Lecture/écriture                                                                             |
| Type           | Bool                                                                                  |
| Default        | Vrai                                                                                  |
| Système minimal | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’ordinateur. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Poste de travail »                                                                                                                                                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Le système d’exploitation installé sur l’ordinateur local.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Type           | Valeurs possibles longues : COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16) |
| Default        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Indique si les partitions COM+ peuvent être utilisées sur l’ordinateur local. Si cette propriété a la valeur false, toute tentative d’utilisation de partitions COM+ génère une erreur. |
| Access         | Lecture/écriture                                                                                                                                               |
| Type           | Bool                                                                                                                                                    |
| Default        | False                                                                                                                                                   |
| Système minimal | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Ports



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne qui décrit les ports utilisés pour l’utilisation d’Internet ou de l’intranet, en fonction de la propriété InternetPortsListed ; par exemple, « 500-599:600-800 ». |
| Access         | Lecture/écriture                                                                                                                                               |
| Type           | String                                                                                                                                                  |
| Valeur par défaut        | ""                                                                                                                                                      |
| Système minimal | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Entrée | Valeur |
|----------------|-------------------------------------|
| Description    | Permet l’utilisation de redistributeurs de ressources. |
| Access         | Lecture/écriture                           |
| Type           | Bool                                |
| Default        | Vrai                                |
| Système minimal | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Contrôle si le proxy IIS RPC est activé. Le proxy IIS RPC est utilisé conjointement avec IIS pour transférer les appels au mécanisme RPC depuis IIS et est l’un des principaux éléments des services Internet COM, qui est activé en affectant à CISEnabled la valeur true. Pour plus d’informations sur RPCProxyEnabled, consultez [sécurité RPC http](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                             |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Default        | False                                                                                                                                                                                                                                                                                                                                                 |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | S’applique aux ordinateurs DCOM qui envoient des appels interprocessus aux méthodes [**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . |
| Access         | Lecture/écriture                                                                                                                                                                 |
| Type           | Bool                                                                                                                                                                      |
| Default        | False                                                                                                                                                                     |
| Système minimal | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Entrée | Valeur |
|----------------|---------------------------------------------------------|
| Description    | Affectez la valeur true si le suivi de sécurité est activé sur les objets. |
| Access         | Lecture/écriture                                               |
| Type           | Bool                                                    |
| Default        | Vrai                                                    |
| Système minimal | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine comment la stratégie de restriction logicielle (SRP) gère les connexions d’activation en tant qu’activateur. Si la valeur est true, le niveau de confiance SRP configuré pour l’objet serveur est comparé au niveau de confiance SRP de l’objet client et le niveau de confiance le plus élevé (plus rigoureux) est utilisé pour exécuter l’objet serveur. Si la valeur est false, l’objet serveur s’exécute avec le niveau de confiance SRP de l’objet client, quel que soit le niveau de confiance du SRP avec lequel le serveur est configuré. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Default        | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Détermine comment la stratégie de restriction logicielle (SRP) gère les tentatives de connexion aux processus existants. Si la valeur est false, les tentatives de connexion aux objets en cours d’exécution ne sont pas vérifiées pour les niveaux de confiance SRP appropriés. Si la valeur est true, l’objet en cours d’exécution doit avoir un niveau de confiance SRP égal ou supérieur à celui de l’objet client. Par exemple, un objet client avec un niveau de confiance SRP non restreint ne peut pas se connecter à un objet en cours d’exécution avec un niveau de confiance SRP interdit. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Default        | Vrai                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Doit être défini sur une valeur suffisante en secondes si vous effectuez de nombreuses opérations au sein d’une transaction. Le délai d’attente par défaut est de 60 secondes et le délai d’expiration maximal est de 3600 secondes (1 heure). L’affectation de la valeur 0 à cette propriété désactive les délais d’expiration de la transaction. Cette propriété peut être remplacée par des composants individuels à l’aide de la propriété ComponentTransactionTimeout de la collection [**Components**](components.md) . |
| Access         | Lecture/écriture                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Type           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Default        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Exemple

l’exemple de Visual Basic Microsoft suivant montre comment se connecter à un ordinateur distant et obtenir sa propriété SecurityTrackingEnabled à l’aide de la collection **LocalComputer** de l’ordinateur distant. pour utiliser cet exemple, ajoutez la bibliothèque de types d’administration COM+ en tant que référence à votre projet Visual Basic.


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’ordinateur distant. le code Visual Basic suivant montre comment se connecter à l’ordinateur nommé « RemoteComputerName ».


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
