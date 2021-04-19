---
description: Utilisation des fichiers de configuration Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Utilisation des fichiers de configuration Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516372"
---
# <a name="using-per-application-configuration-files"></a>Utilisation des fichiers de configuration Per-Application

L’utilisation de fichiers de configuration par application COM+ requiert les étapes de base suivantes :

-   Configurez un répertoire racine d’application pour une application COM+.
-   Créez les fichiers application. manifest et application.config dans le répertoire racine de l’application COM+.

> [!Note]  
> Les fichiers de configuration par application sont disponibles uniquement à partir de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.

 

**Pour utiliser un fichier de configuration par application**

1.  Créez une bibliothèque de classes .NET, avec une référence à l’assembly System. EnterpriseServices.

2.  La bibliothèque de classes doit contenir le code suivant :

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    Notez que « ConfigData1 » est un exemple de nom de paramètre. Vous pouvez remplacer ceci par le nom du paramètre de votre choix.

3.  Créez une application COM+ vide. Pour obtenir des instructions sur la procédure à suivre, consultez [création d’une application com+](creating-a-new-com--application.md).
4.  Installez la bibliothèque de classes que vous avez créée dans l’application COM+. Pour obtenir des instructions sur la procédure à suivre, consultez [installation de nouveaux composants](installing-new-components.md).
5.  Dans l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ que vous avez créée, puis sélectionnez **Propriétés**.
6.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **activation** .
7.  Assurez-vous que le **type d’activation** est défini sur **application serveur**.
8.  Dans la zone de texte **répertoire racine** de l’application, entrez le chemin d’accès ou accédez au répertoire dans lequel vous souhaitez stocker vos fichiers de configuration d’application pour cette application.
9.  Cliquez sur **OK**.

    Notez que vous pouvez également spécifier le répertoire racine de l’application COM+ à l’aide de la propriété ApplicationDirectory de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Pour plus d’informations, consultez [**applications**](applications.md).

10. Dans le répertoire que vous avez choisi pour stocker vos fichiers de configuration d’application, créez un fichier nommé *application*. manifest. Avec un éditeur de texte, ajoutez le texte suivant à ce fichier :

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. Dans le même répertoire, créez un fichier nommé *application*. config. Avec un éditeur de texte, ajoutez le texte suivant à ce fichier :

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Notez que ce fichier de configuration n’est qu’un exemple. Vous pouvez créer plusieurs clés avec des noms et des valeurs différents. Notez, toutefois, que « ConfigData1 » correspond au nom de paramètre utilisé dans la bibliothèque de classes créée précédemment.

12. Créez une application console .NET, avec une référence à la bibliothèque de classes .NET que vous avez créée précédemment et une référence à l’assembly System. EnterpriseServices.
13. L’application console doit contenir le code suivant :
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

Exécutez l’application console. La sortie doit être :

``` syntax
Configuration Data Number 1
```

 

 



