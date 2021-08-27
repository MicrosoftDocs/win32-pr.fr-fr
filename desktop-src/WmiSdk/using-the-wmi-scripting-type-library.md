---
description: vous pouvez utiliser la bibliothèque de types de scripts wmi pour appeler les méthodes de l’API de script wmi à partir de Microsoft Visual Studio et dans Windows fichiers WSF de l’hôte de script.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Utilisation de la bibliothèque de types de scripts WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20e5a2aa10bccfbd91b003f1db120691b6c61bb4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881179"
---
# <a name="using-the-wmi-scripting-type-library"></a>Utilisation de la bibliothèque de types de scripts WMI

vous pouvez utiliser la bibliothèque de types de scripts wmi pour appeler les méthodes de l’API de script wmi à partir de Microsoft Visual Studio et dans Windows fichiers WSF de l’hôte de script.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Utilisation de la bibliothèque de types de scripts WMI avec Microsoft Visual Studio

> [!Note]  
> les fonctionnalités de Visual InterDev 6,0 ont été intégrées à [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).

 

La procédure suivante décrit comment permettre à l’environnement de développement intégré (IDE) d’être conscient de la bibliothèque de types WbemScripting.

**Pour ajouter la bibliothèque de types de scripts WMI aux références de projet**

1.  sélectionnez **ajouter des références** dans le menu **Project** .
2.  Dans l’onglet COM de la zone **Ajouter une référence** , sélectionnez Bibliothèque de scripts Microsoft WMI v 1.2.
3.  Si aucune option appropriée n’apparaît dans la liste Références, ajoutez-la à l’aide de l’option **Parcourir** dans la zone **références** . L' **exploration** ouvre une zone **Ajouter une référence** qui vous permet de rechercher la bibliothèque de types WbemScripting.

    La bibliothèque de types WbemScripting réside dans le fichier wbemdisp. tlb dans le répertoire% windir% \\ system32 \\ WBEM.

4.  Sélectionnez le fichier et cliquez sur **Ouvrir**. La bibliothèque Microsoft WMI Scripting V 1.2 apparaît dans la liste des références. Veillez à activer la case à cocher en regard de cet élément dans la liste.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>utilisation de la bibliothèque de types de scripts WMI avec Windows script Host 2,0

vous pouvez inclure la référence à **WbemScripting. SWbemLocator** dans un fichier Windows script Host WSF, contrairement à un script écrit dans Visual Basic, l’édition de script ou d’autres langages de script. Cela vous permet d’utiliser des noms de constantes au lieu de valeurs. Par exemple, utilisez **WbemAuthenticationLevelPktPrivacy** plutôt que la valeur 6 lors de la définition de l’authentification.

Les scripts peuvent se connecter à l’API de script pour la bibliothèque de types WMI à l’aide des méthodes suivantes :

-   Spécification du GUID WbemScripting dans les méthodes VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) et [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    cette alerte Windows hôte de Script pour se connecter au jeu d’objets WMI.

    L’exemple de code VBScript suivant crée un nouvel objet [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Utilisation de la [chaîne de moniker](constructing-a-moniker-string.md) « winmgmts : » lors de l’obtention d’un objet nouveau ou existant.

    L’exemple de code VBScript suivant utilise le moniker « winmgmts : » pour obtenir l’instance [**du \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) avec une propriété **handle** égale à 0 (zéro). **Descripteur** est la propriété de clé pour cette classe.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Référencement de la bibliothèque de types WMI à l’aide &lt; &gt; de la balise de référence du format de fichier XML WSH 2,0. Si vous utilisez la &lt; &gt; balise de référence, la balise doit avoir soit un attribut **UUID** dont la valeur est le **GUID** de la bibliothèque de types WMI, soit (recommandé) un attribut d’objet dont la valeur est le **ProgID** de l’un des objets de script WMI que vous pouvez créer.

    L’exemple de code VBScript suivant utilise le PROGID « WbemScripting ». Pour exécuter le script, enregistrez le texte dans un fichier avec une extension. wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Utilisation d’une balise d'> **objet** <pour créer un objet de script WMI. Vous pouvez spécifier l’attribut **ID** avec la valeur d’un nom qui fait référence à l’objet de script WMI que vous souhaitez créer, et l’attribut **ProgID** égal à PROID de l’objet de script WMI.

    Le script WSH suivant affiche le nom d’hôte et le nombre de processeurs sur l’ordinateur local. Pour exécuter le script, enregistrez le texte dans un fichier avec une extension. wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API de script pour WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
