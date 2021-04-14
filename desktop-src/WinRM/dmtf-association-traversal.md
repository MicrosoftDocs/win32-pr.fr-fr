---
title: Découverte de profil DMTF par traversée d’association
description: Un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383075"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Découverte de profil DMTF par traversée d’association

Un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système. Le modèle est conforme à un standard géré par la[DMTF](https://www.dmtf.org/standards/wsman)(Desktop Management Task Force) et est connu comme le Common Information Model (CIM). Certaines classes du modèle, telles que le [ \_ fichier de fichier CIM](../cimwin32prov/cim-datafile.md) ou le [ \_ processus Win32](../cimwin32prov/win32-process.md), correspondent directement aux entités gérables. D’autres classes du modèle, telles que [Win32 \_ SystemServices](../cimwin32prov/win32-systemservices.md), représentent les relations entre les entités gérables. Ces classes de modélisation des relations sont appelées des classes d’association.

À l’aide du langage de requête spécifique à WMI, WQL, vous pouvez récupérer des instances de classes qui représentent des entités gérables ou des instances de classes d’association. Toutefois, WQL est spécifique à l’implémentation. Il fonctionne uniquement avec l’implémentation Windows de la norme DMTF (WMI). En outre, la syntaxe WQL pour la récupération des classes d’association est plutôt compliquée.

L’infrastructure Windows Remote Management (WinRM) offre un excellent moyen de tirer parti des fonctionnalités de WMI. Les premières versions de WinRM devaient utiliser WQL pour extraire des instances de classes d’association. WinRM 2,0 intègre une nouvelle fonctionnalité appelée détection de profil DMTF par traversée d’association. La traversée d’association permet à un utilisateur de WinRM de récupérer des instances de classes d’association à l’aide d’un mécanisme de filtrage standard, le dialecte AssociationFilter, défini dans la spécification de liaison CIM DMTF. Pour plus d’informations sur le parcours d’association, consultez la spécification de liaison CIM WS-Management ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

L’utilitaire WinRM fournit un mécanisme simple pour parcourir l’Association appropriée et récupérer un profil d’appareil.

## <a name="configuration-implementation-details"></a>Détails de l’implémentation de la configuration

L’utilitaire WinRM prend désormais en charge un dialecte pour la demande d’association. L’URI ou l’alias peut être spécifié à l’aide de l’utilitaire WinRM.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| association | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Récupération des instances d’une classe d’association à l’aide du dialecte AssociationFilter

L’utilitaire WinRM peut récupérer les instances de classe d’association WMI d’une instance source particulière. La commande suivante montre comment utiliser l’utilitaire WinRM pour récupérer des instances de classes d’association de [ \_ service Win32](../cimwin32prov/win32-service.md) . Le commutateur « -associations » doit être utilisé pour retourner des classes d’association.

**WinRM Enumerate wmicimv2/ \* -Dialect : Association-associations-filtre : {Object = Win32 \_ Service ? Name = WinRM ; resultclassname = Win32 \_ dependentservice ; Role = dependent}**

L’extrait de code textuel suivant est la sortie de la commande ci-dessus :

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Récupération des instances d’une classe associée à l’aide du dialecte AssociationFilter

L’utilitaire WinRM peut récupérer les instances de classe WMI associées à une instance source particulière. La commande suivante montre comment utiliser l’utilitaire WinRM pour récupérer les instances des classes associées au [ \_ service Win32](../cimwin32prov/win32-service.md) .

**WinRM Enumerate wmicimv2/ \* -Dialect : Association-filtre : {Object = Win32 \_ Service ? Name = WinRM ; associationclassname = Win32 \_ dependentservice ; resultclassname = Win32 \_ service ; ResultRole = Antecedent ; Role = dependent}**

L’extrait de code textuel suivant est la sortie de la commande ci-dessus :

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 