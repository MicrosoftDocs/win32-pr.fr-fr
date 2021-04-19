---
description: Avant d’implémenter votre fournisseur, vous devez d’abord inscrire votre fournisseur auprès de WMI. L’inscription du fournisseur définit le type du fournisseur et les classes que le fournisseur prend en charge. WMI ne peut accéder qu’aux fournisseurs inscrits.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Inscription d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536735"
---
# <a name="registering-a-provider"></a>Inscription d’un fournisseur

Avant d’implémenter votre fournisseur, vous devez d’abord inscrire votre fournisseur auprès de WMI. L’inscription du fournisseur définit le type du fournisseur et les classes que le fournisseur prend en charge. WMI ne peut accéder qu’aux fournisseurs inscrits.

> [!Note]  
> Pour plus d’informations sur l’inscription d’un fournisseur MI, consultez [procédure : inscrire un fournisseur mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Vous pouvez écrire votre code de fournisseur avant d’inscrire le fournisseur. Toutefois, il est très difficile de déboguer un fournisseur qui n’est pas inscrit auprès de WMI. La détermination des interfaces pour votre fournisseur vous aide également à décrire l’objectif et la structure d’un fournisseur. Par conséquent, l’inscription de votre fournisseur vous aide à concevoir votre fournisseur.

Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur.

Un fournisseur doit être inscrit pour tous les différents types de fonctions fournisseur qu’il exécute. Presque tous les fournisseurs fournissent des instances de classes qu’ils définissent, mais ils peuvent également fournir des données de propriété, des méthodes, des événements ou des classes. Le fournisseur peut également être inscrit en tant que fournisseur de consommateur d’événements ou que fournisseur de compteur de performance. Il est recommandé de combiner toutes les fonctionnalités du fournisseur dans un fournisseur plutôt que d’avoir plusieurs fournisseurs distincts pour chaque type. Par exemple, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider), qui fournit des méthodes et des instances, et le [fournisseur de quota de disque](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), qui fournit des instances, des méthodes et des événements.

Un fournisseur doit être inscrit pour tous les différents types de fonctions fournisseur qu’il exécute. Presque tous les fournisseurs fournissent des instances de classes qu’ils définissent, mais ils peuvent également fournir des données de propriété, des méthodes, des événements ou des classes. Le fournisseur peut également être inscrit en tant que fournisseur de consommateur d’événements ou que fournisseur de compteur de performance.

La même instance de [**\_ \_ Win32Provider**](--win32provider.md) est utilisée pour chaque type d’inscription :

-   [Inscription d’un fournisseur d’instances](registering-an-instance-provider.md)
-   [Inscription d’un fournisseur de classe](registering-a-class-provider.md)
-   [Inscription d’un fournisseur de méthode](registering-a-method-provider.md)
-   [Inscription d’un fournisseur d’événements](registering-an-event-provider.md)
-   [Inscription d’un fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md)
-   [Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Exemple : création et inscription d’une instance d’un fournisseur

L’exemple suivant montre un fichier MOF qui crée et inscrit une instance du fournisseur de [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) dans l’espace de \\ noms CIMV2 racine. Il affecte l’alias $Reg au fournisseur afin d’éviter le nom de chemin d’accès long requis dans les inscriptions d’instance et de méthode. Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md).

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>Exemple : inscription d’un fournisseur

La procédure suivante décrit comment inscrire un fournisseur.

**Pour inscrire un fournisseur**

1.  Inscrivez le fournisseur en tant que serveur COM.

    Si nécessaire, vous devrez peut-être créer des entrées de registre. Ce processus s’applique à tous les serveurs COM et n’est pas lié à WMI. Pour plus d’informations, consultez la section COM dans la documentation du kit de développement logiciel (SDK) Microsoft Windows.

2.  Créez un fichier MOF qui contient des instances de [**\_ \_ Win32Provider**](--win32provider.md) et une instance d’une classe dérivée directement ou indirectement de [**\_ \_ ProviderRegistration**](--providerregistration.md), telle que [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant des instances de classes dérivées de **\_ \_ Win32Provider** ou [**\_ \_ ProviderRegistration**](--providerregistration.md).
3.  Définissez le [**HostingModel**](--win32provider.md) dans l’instance de **\_ \_ Win32Provider** en fonction des valeurs des [modèles d’hébergement](provider-hosting-and-security.md).

    > [!Note]  
    > À moins que le fournisseur n’ait besoin des privilèges élevés du compte LocalSystem, la propriété [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) doit avoir la valeur « NetworkServiceHost ». Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

     

    L’exemple MOF suivant tiré de l’exemple complet montre le code qui crée une instance de [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Instance d’une classe dérivée directement ou indirectement de [**\_ \_ ProviderRegistration**](--providerregistration.md), pour décrire l’implémentation logique du fournisseur. Un fournisseur peut être inscrit pour plusieurs types de fonctionnalités différents. L’exemple ci-dessus inscrit RegProv en tant que fournisseur d’instance et de méthode. Toutefois, si RegProv prend en charge la fonctionnalité, il peut également être enregistré en tant que propriété ou fournisseur d’événements. Le tableau suivant répertorie les classes qui inscrivent les fonctionnalités du fournisseur.

    

    | Classes d’inscription du fournisseur                                                        | Description                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Inscrit un [fournisseur d’instances](registering-an-instance-provider.md).             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Inscrit un [fournisseur d’événements](registering-an-event-provider.md).                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Inscrit un [fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md). |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Inscrit un [fournisseur de méthode](registering-an-event-consumer-provider.md).          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Inscrit un [fournisseur de propriétés](registering-a-property-provider.md).               |

    

     

5.  Placez le fichier MOF dans un répertoire permanent.

    En règle générale, vous devez placer le fichier dans le répertoire d’installation du fournisseur.

6.  Compilez le fichier MOF à l’aide de [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

    **Windows 8 et Windows Server 2012 :** Lors de l’installation des fournisseurs, [**mofcomp**](mofcomp.md) et l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) traitent les \[ \] \[ qualificateurs Key et static \] comme true s’ils sont présents, indépendamment de leurs valeurs réelles. D’autres qualificateurs sont considérés comme false s’ils sont présents, mais ne sont pas explicitement définis sur true.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> </dl>

 

 
