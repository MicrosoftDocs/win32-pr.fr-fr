---
title: Windows Gestion à distance et WMI
description: Windows la gestion à distance peut être utilisée pour récupérer les données exposées par Windows Management Instrumentation.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642469"
---
# <a name="windows-remote-management-and-wmi"></a>Windows Gestion à distance et WMI

Windows la gestion à distance peut être utilisée pour récupérer les données exposées par Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) et [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)). Vous pouvez obtenir des données WMI avec des scripts ou des applications qui utilisent l' [API de script WinRM](winrm-scripting-api.md) ou via l’outil en ligne de commande **WinRM** .

WinRM prend en charge la plupart des opérations et classes WMI familières, y compris les objets incorporés. WinRM peut tirer parti de WMI pour collecter des données sur les [*ressources*](windows-remote-management-glossary.md) ou pour gérer les ressources sur un système d’exploitation basé sur Windows. Cela signifie que vous pouvez obtenir des données sur des objets tels que des disques, des cartes réseau, des services ou des processus de votre entreprise par le biais de l’ensemble existant de [classes WMI](/windows/desktop/WmiSdk/wmi-classes). Vous pouvez également accéder aux données matérielles disponibles à partir du [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI standard.

## <a name="identifying-a-wmi-resource"></a>Identification d’une ressource WMI

Vous pouvez référencer une classe WMI en tant que [*ressource*](windows-remote-management-glossary.md) dans WinRM et dans le protocole WS-Management : un type d’entité gérée, comme un service ou un disque.

Une classe ou une méthode WMI est identifiée par un [*URI*](windows-remote-management-glossary.md), tout comme n’importe quelle autre ressource lorsque vous utilisez le protocole WS-Management. L’URI peut spécifier une ressource WMI (classe), une action WMI (méthode) ou identifier une instance spécifique d’une classe dans [*les messages*](windows-remote-management-glossary.md) envoyés sur un réseau. Pour plus d’informations, consultez [URI de ressource](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Construction du préfixe URI pour les classes WMI

Le préfixe URI contient une partie fixe et l’espace de noms WMI. par exemple, le préfixe URI dans Windows serveur qui contient la partie fixe du préfixe est : `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Cela permet de générer le préfixe URI pour n’importe quel espace de noms WMI. Par exemple, pour accéder à l’espace de noms WMI **\\ par défaut racine** , utilisez le préfixe URI suivant : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

La majorité des classes WMI pour la gestion se trouvent dans l’espace de noms **\\ cimv2 racine** . Pour accéder aux classes et aux instances dans l’espace de noms **\\ cimv2 racine** , utilisez le préfixe URI : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Pour plus d’informations, consultez [URI de ressource](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Génération d’un URI complet pour les classes WMI

L’URI que vous fournissez, soit à l’outil de ligne de commande **WinRM** , soit à un script, se compose du préfixe et de la spécification de ressource.

La procédure suivante décrit comment générer un URI de ressource pour obtenir une classe WMI ou pour l’utiliser dans une opération d’énumération.

**Pour générer un URI de ressource pour une classe WMI**

1.  Commencez par le préfixe qui indique que le schéma de protocole WS-Management doit être utilisé.

    https://schemas.microsoft.com/wbem/wsman/1

    Le préfixe URI de ressource pour les classes WMI est toujours identique. Pour plus d’informations, consultez [préfixes d’URI](uri-prefixes.md).

2.  Ajoutez l’espace de noms WMI au préfixe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Ajoutez le nom de la classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Pour définir la valeur d’une propriété, ou pour appeler une méthode spécifique, ajoutez la ou les valeurs de clé requises pour la classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Si vous laissez la valeur de clé vide, vous ne modifierez pas la valeur de la propriété d’origine.

    > [!Note]  
    > Si vous laissez la valeur de clé vide, la valeur de la propriété est définie sur **null**.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Recherche d’une ressource WMI avec WinRM

vous pouvez obtenir des données WMI via l’outil en ligne de commande, **Winrm** ou via un script Visual Basic qui utilise l' [API de script winrm](winrm-scripting-api.md). Vous n’utilisez pas de [chemin d’accès WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) pour rechercher une ressource. Au lieu de cela, vous convertissez l’espace de noms WMI et la hiérarchie en un [*URI*](windows-remote-management-glossary.md).

L’URI WinRM pour une classe WMI contient deux parties : le [préfixe URI](uri-prefixes.md) et la classe à laquelle vous souhaitez accéder.

Par exemple, l’URI suivant peut être fourni à la méthode [**session. Enumerate**](session-enumerate.md) pour répertorier tous les services sur un ordinateur. Le préfixe URI est `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , et la classe [**est \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

Dans WMI, répertoriez les données de toutes les instances d’une ressource ou d’une classe de plusieurs façons :

-   Une requête pour toutes les instances de cette ressource.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Un appel à [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) ou [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

Dans WinRM, il existe une méthode pour répertorier toutes les instances d’une ressource : [**session. Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Recherche d’une instance spécifique d’une ressource WMI

Dans WMI, vous pouvez désigner une instance particulière d’une classe en spécifiant des valeurs pour les propriétés de clé ou en interrogeant une instance qui correspond à une liste de valeurs de propriété. Les propriétés de clé ont le [**qualificateur de clé**](/windows/desktop/WmiSdk/key-qualifier)WMI.

Vous pouvez obtenir une instance spécifique d’une classe de plusieurs façons :

-   Un appel à [**session. Enumerate**](session-enumerate.md) avec les paramètres de *filtre* et de *dialecte* pour créer une requête.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Un appel à [**SWbemServices. obtenir**](/windows/desktop/WmiSdk/swbemservices-get). Pour [**session. obtenir**](session-get.md), vous devez fournir une ou plusieurs valeurs de clés spécifiques, précédées d’un point d’interrogation ( ?).

    Le format de l’URI pour une instance spécifique est `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Une classe WMI peut avoir plusieurs clés. Les paires nom-valeur de clé sont séparées par un signe « + ». Dans ce cas, le format est : `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    La syntaxe WinRM pour obtenir un objet WMI Singleton est différente de WMI. Un singleton est une classe WMI définie de sorte qu’une seule instance est autorisée. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) ou [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sont des exemples de classe singleton WMI.

    La syntaxe WMI pour les singletons est présentée dans l’exemple de code VBScript suivant.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    L’exemple suivant illustre la syntaxe du singleton WinRM qui n’utilise pas « @ ».

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Ajout d’un [*Sélecteur*](windows-remote-management-glossary.md) à un objet [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .

    L’exemple de code VBScript suivant montre comment utiliser un sélecteur pour obtenir une instance spécifique du [**\_ processeur Win32**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Préfixes d’URI](uri-prefixes.md)
</dt> <dt>

[URI de ressource](resource-uris.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> </dl>
