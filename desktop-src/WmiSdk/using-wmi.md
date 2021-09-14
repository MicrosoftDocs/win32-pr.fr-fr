---
description: Feuille de route pour l’utilisation de WMI pour obtenir des données pour les applications et les scripts clients ou pour fournir des données à WMI à partir d’une application.
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: Utilisation de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d1556d321441c7e6a3191bf95e85db356e7ba9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118501"
---
# <a name="using-wmi"></a>Utilisation de WMI

Vous pouvez utiliser WMI à partir d’applications clientes et de scripts. Il fournit une infrastructure qui facilite la découverte et l’exécution de tâches de gestion. En outre, vous pouvez ajouter à l’ensemble des tâches de gestion possibles en créant vos propres fournisseurs WMI.

> [!Note]  
> la nouvelle génération de WMI pour l’écriture d’applications et de scripts est disponible par le biais de l’Infrastructure de gestion Windows (MI). Pour plus d’informations, consultez [fournisseurs et clients mi](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).

 

Les rubriques suivantes sont présentées dans cette section :

-   [Obtention de données à partir de WMI](#obtaining-data-from-wmi)
-   [Fourniture de données à WMI](#providing-data-to-wmi)
-   [Tâches importantes pour WMI](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a>Obtention de données à partir de WMI

La procédure suivante décrit comment obtenir des données à partir de WMI en écrivant un script ou une application.

**Pour obtenir des données à partir de WMI en écrivant un script ou une application**

1.  Choisissez la langue à utiliser. Pour plus d’informations sur les scripts, consultez [création d’un script WMI](creating-a-wmi-script.md). Pour plus d’informations sur C++, consultez [création d’une application WMI à l’aide de c++](creating-a-wmi-application-using-c-.md). Pour plus d’informations sur C# ou WMI .NET, consultez [vue d’ensemble de WMI .net](/previous-versions/).

    Vous pouvez afficher ou manipuler des données WMI dans de nombreuses langues. Le tableau suivant répertorie les rubriques qui décrivent comment utiliser les langages de script et d’application pour obtenir des données.

    

    
| Langue de l’application | Rubrique | 
|----------------------|-------|
| scripts écrits en Microsoft ActiveX script hosting, y compris Visual Basic scripting Edition (VBScript) et Perl<br /> | <a href="scripting-api-for-wmi.md">API de script pour WMI</a>.<br /> Commencez par <a href="creating-a-wmi-script.md">créer un script WMI</a>.<br /> Pour obtenir des exemples de code de script, consultez <a href="wmi-tasks-for-scripts-and-applications.md">tâches WMI pour les scripts et les applications</a> et le référentiel de scripts TechNet <a href="https://www.microsoft.com/technet/scriptcenter">scriptcenter</a> .<br /> | 
| Windows PowerShell<br /> | <a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Prise en main avec Windows PowerShell</a><br /> Applets de commande PowerShell WMI, telles que la commande <a href="/previous-versions//dd315295(v=technet.10)">-WmiObject</a>.<br /> | 
| applications Visual Basic<br /> | <a href="scripting-api-for-wmi.md">API de script pour WMI</a>.<br /> | 
| pages ASP (Active Server Page)<br /> | <a href="scripting-api-for-wmi.md">API de script pour WMI</a>.<br /> Commencez par <a href="creating-active-server-pages-for-wmi.md">créer des pages de Active Server pour WMI</a>.<br /> | 
| applications C++<br /> | <a href="com-api-for-wmi.md">API com pour WMI</a>.<br /> Commencez par <a href="creating-a-wmi-application-using-c-.md">créer une application WMI à l’aide</a> d’exemples d’applications C++ et <a href="wmi-c---application-examples.md">WMI c++</a> (contient des exemples).<br /> | 
| .NET Framework les applications écrites en C#, Visual Basic .net ou J #<br /> | Classes dans l’espace de noms <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. infrastructure</strong></a> .<br /><blockquote>    [!Note]<br /><strong>System. Management</strong> était l’espace de noms d’origine qui traitait du code MANAGÉ pour WMI. Toutefois, la technologie sous-jacente pour <strong>System. Management</strong> est généralement plus lente que, et n’est pas mise à l’échelle, ni à <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft. Management. infrastructure</strong></a>. Par conséquent, il n’est pas recommandé d’utiliser <strong>System. Management</strong> pour les nouveaux projets. (Pour plus d’informations sur <strong>System. Management</strong>, consultez <a href="/previous-versions/bb404655(v=vs.90)">vue d’ensemble de WMI .net</a>.)    </blockquote><br /> | 


    

     

2.  Assurez-vous que vos connexions aux ordinateurs distants fonctionnent.

    Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

3.  La connexion à WMI sur des ordinateurs distants requiert des paramètres de sécurité corrects, comme expliqué dans [maintenance de la sécurité WMI](maintaining-wmi-security.md). Le tableau suivant répertorie les rubriques qui décrivent comment configurer les paramètres de sécurité avec les scripts et les langues de l’application.

    

    | Langage                                                      | Rubrique                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Scripts dans n’importe quel langage, Visual Basic applications<br/> | [Définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | pages ASP (Active Server Page)<br/>                                | [Configuration d’IIS 5 et versions ultérieures pour les scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | C++<br/>                                                | [Définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md) et [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)<br/> |

    

     

4.  Après vous être connecté à WMI, vous pouvez obtenir des données via des requêtes et des énumérations.

    Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md) et [interrogation avec WQL](querying-with-wql.md).

5.  Les données du Registre sont disponibles via WMI et vous pouvez créer des clés et des valeurs ou en modifier.

    Pour plus d’informations, consultez [modification du Registre système](modifying-the-system-registry.md).

6.  Vous pouvez vous abonner aux notifications d’événements via WMI, soit temporairement entre les redémarrages du système, soit définitivement.

    Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md) et [réception d’un événement WMI](receiving-a-wmi-event.md).

7.  Les données des compteurs de performances d’un système sont disponibles via WMI.

    Les compteurs de la bibliothèque de performances système sont convertis en classes WMI. Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md).

8.  [Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md) décrit comment effectuer de nombreuses tâches d’administration avec WMI.

## <a name="providing-data-to-wmi"></a>Fourniture de données à WMI

La procédure suivante décrit comment fournir des données à WMI en écrivant un fournisseur.

**Pour fournir des données à WMI en écrivant un fournisseur**

-   Déterminez le type de fournisseur à écrire.

    Vous ne pouvez pas écrire un fournisseur WMI dans VBScript. Toutefois, vous pouvez prendre plusieurs autres approches pour l’écriture d’un fournisseur COM WMI :

    -   À l’aide de l’Assistant ATL WMI dans Visual Studio.

        Cette approche crée un fournisseur COM non managé. Pour plus d’informations, consultez [Ajout d’un fournisseur d’instances WMI](./writing-an-instance-provider.md) et [Ajout d’un fournisseur d’événements WMI](./writing-an-event-provider.md).

    -   Utilisation directe de COM dans n’importe quel environnement de développement intégré.

        Cette approche crée un fournisseur COM non managé.

    -   à l’aide de WMI dans l' .NET Framework pour créer un fournisseur de code managé.

        Cette approche crée un fournisseur de code managé. les fournisseurs de code managé peuvent être écrits dans n’importe quel langage de .NET Framework, sont plus simples à écrire que les fournisseurs COM wmi et peuvent obtenir des données à partir des classes wmi [*CIM*](gloss-c.md), telles que les [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider). toutefois, le fournisseur WMI .NET Framework présente certaines limitations. Pour plus d’informations, consultez [gestion des applications à l’aide de WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).

    -   L’utilisation des classes de l' [infrastructure du fournisseur](wmi-c-classes.md) n’est pas recommandée.

        l’infrastructure de fournisseur a été remplacée par les assistants WMI ATL, à l’aide de COM directement, ou .NET Framework fournisseurs. La création d’un fournisseur COM WMI avec les classes de l’infrastructure du fournisseur n’est plus recommandée. le tableau suivant répertorie les rubriques qui décrivent comment utiliser les fournisseurs COM ou .NET Framework.

    

    | Fournisseur                                                      | Rubrique                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | Fournisseur COM dans le même processus que WMI<br/>            | [Fourniture de données à WMI](providing-data-to-wmi.md)<br/>                                           |
    | Fournisseur découplé COM<br/>                             | [Incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md)<br/> |
    | fournisseur .NET Framework en C# ou Visual Basic .net<br/> | [Gestion des applications à l’aide de WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))<br/>            |

    

     

## <a name="important-tasks-for-wmi"></a>Tâches importantes pour WMI

Les rubriques suivantes fournissent des informations sur l’utilisation de WMI pour surveiller et contrôler les composants d’entreprise.



| Rubrique                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | Décrit comment trouver la classe et les procédures WMI appropriées à utiliser dans les scripts et les applications qui effectuent des tâches d’administration réseau et d’ordinateur courantes, telles que l’ajout d’une nouvelle connexion d’imprimante pour un ordinateur distant ou la recherche de tous les correctifs logiciels installés sur un ordinateur.<br/>                                                                            |
| [Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)<br/>                                                     | tout langage de script, tel que VBScript ou Perl, qui fonctionne avec des objets ActiveX peut accéder aux données WMI. les Applications peuvent accéder à wmi en C++, à l’aide [de l’api COM pour wmi](com-api-for-wmi.md) ou dans Visual Basic, à l’aide de la[bibliothèque de types](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb et de l' [api de script pour wmi](scripting-api-for-wmi.md).<br/> |
| [Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | Décrit comment les scripts, les applications et les fournisseurs peuvent établir des connexions à WMI sur des ordinateurs distants pour obtenir des données ou contrôler le matériel et les logiciels.<br/>                                                                                                                                                                                                   |
| [Connexion à WMI sur un ordinateur distant à l’aide de Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | décrit comment utiliser Windows PowerShell pour établir des connexions à WMI sur des ordinateurs distants afin d’obtenir des données ou de contrôler le matériel et les logiciels.<br/>                                                                                                                                                                                                            |
| [Événements d’analyse](monitoring-events.md)<br/>                                                                                           | Décrit comment recevoir des notifications d’événements en créant des consommateurs d’événements WMI temporaires ou permanents.<br/>                                                                                                                                                                                                                                                           |
| [Fourniture de données à WMI](providing-data-to-wmi.md)<br/>                                                                                   | WMI fournit des données de gestion dynamique aux scripts et applications clients en les obtenant auprès des fournisseurs.<br/>                                                                                                                                                                                                                                                    |
| [Obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | Décrit comment accéder aux fournisseurs et aux éléments à prendre en compte par défaut pour les writers de fournisseur sur les systèmes 64 bits.<br/>                                                                                                                                                                                                                                                    |



