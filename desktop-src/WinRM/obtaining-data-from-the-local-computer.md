---
title: Obtention de données à partir de l’ordinateur local
description: Bien que Windows Remote Management et WS-Management protocole soient explicitement conçus pour la communication à distance, l’établissement d’une session sur l’ordinateur local est le cas le plus simple.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727405"
---
# <a name="obtaining-data-from-the-local-computer"></a>Obtention de données à partir de l’ordinateur local

Bien que Windows Remote Management et WS-Management protocole soient explicitement conçus pour la communication à distance, l’établissement d’une session sur l’ordinateur local est le cas le plus simple. Certains scripts peuvent nécessiter des données d’accès sur l’ordinateur local, ainsi que sur des ordinateurs distants.

**WinRM version 2,0 :  **

Toutes les opérations sont considérées comme distantes et le service WinRM doit être démarré avant l’exécution d’une opération. Si une destination distante n’est pas spécifiée, l’hôte local est utilisé par défaut, et toutes les opérations sont envoyées au service WinRM local. Pour plus d’informations sur le démarrage du service WinRM, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

Lors de l’utilisation du service WinRM pour les opérations locales, les facteurs suivants doivent être pris en compte :

-   La configuration WinRM locale ne peut être lue que par les administrateurs.
-   Les autorisations Remote Enable doivent être définies pour les espaces de noms WMI. Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](../wmisdk/securing-a-remote-wmi-connection.md).
-   Si aucun [*écouteur*](windows-remote-management-glossary.md) WinRM n’est créé, le service WinRM écoute les demandes locales sur le port 47001.

Chaque script WinRM doit commencer par l’établissement d’une session ou d’une connexion à un ordinateur en créant un objet de [**session**](session.md) . Une fois la session créée, vous pouvez utiliser les méthodes d’objet de **session** , telles que [**session. Enumerate**](session-enumerate.md) ou [**session. Invoke**](session-invoke.md) pour obtenir des données ou exécuter des méthodes.

La création d’une session est quelque peu similaire à la [connexion](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) à un espace de noms Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)). La session est essentiellement une couche qui vous permet d’envoyer et de recevoir des données par le biais de messages [*SOAP*](windows-remote-management-glossary.md) et du protocole WS-Management. Pour plus d’informations, consultez [protocole WS-Management](ws-management-protocol.md).

L’appel de la méthode [**WSMan. CreateSession**](wsman-createsession.md) pour créer un objet de [**session**](session.md) démarre une [*session*](windows-remote-management-glossary.md) qui se connecte au WinRM local.

**Pour créer une session WSMan et obtenir des données**

1.  Créez un objet [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Créez une session en appelant la méthode [**WSMan. CreateSession**](wsman-createsession.md) . Cette session s’exécute sous votre nom d’utilisateur et votre mot de passe d’ouverture de session et peut obtenir des données via le WinRM local.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Créez un [*URI*](windows-remote-management-glossary.md) de ressource pour identifier la [*ressource*](windows-remote-management-glossary.md) que vous souhaitez gérer ou pour laquelle vous souhaitez obtenir des données. Pour plus d’informations sur la mise en forme d’un URI, consultez [URI de ressource](resource-uris.md). Cet URI de ressource est destiné à une instance spécifique de la classe de [**\_ service WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , le service WinMgmt. Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Appeler des méthodes de [**session**](session.md) qui obtiennent ou énumèrent des données à l’aide de l’URI de ressource. Pour plus d’informations, consultez [API de script WinRM](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Pour obtenir ou gérer des données à partir d’un autre ordinateur ou utiliser différentes méthodes d’authentification, consultez [obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md).

L’exemple de code VBScript suivant montre le script complet qui obtient l’instance spécifique du service WMI [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) nommé « winmgmt ».


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



L’exemple de code VBScript suivant montre le script complet avec la transformation de données. Pour plus d’informations, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Référence Windows Remote Management](windows-remote-management-reference.md)
</dt> </dl>

 

 