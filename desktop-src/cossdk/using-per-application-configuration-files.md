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
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="337ca-103">Utilisation des fichiers de configuration Per-Application</span><span class="sxs-lookup"><span data-stu-id="337ca-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="337ca-104">L’utilisation de fichiers de configuration par application COM+ requiert les étapes de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="337ca-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="337ca-105">Configurez un répertoire racine d’application pour une application COM+.</span><span class="sxs-lookup"><span data-stu-id="337ca-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="337ca-106">Créez les fichiers application. manifest et application.config dans le répertoire racine de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="337ca-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="337ca-107">Les fichiers de configuration par application sont disponibles uniquement à partir de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="337ca-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="337ca-108">**Pour utiliser un fichier de configuration par application**</span><span class="sxs-lookup"><span data-stu-id="337ca-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="337ca-109">Créez une bibliothèque de classes .NET, avec une référence à l’assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="337ca-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="337ca-110">La bibliothèque de classes doit contenir le code suivant :</span><span class="sxs-lookup"><span data-stu-id="337ca-110">The class library should contain the following code:</span></span>

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

    

    <span data-ttu-id="337ca-111">Notez que « ConfigData1 » est un exemple de nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="337ca-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="337ca-112">Vous pouvez remplacer ceci par le nom du paramètre de votre choix.</span><span class="sxs-lookup"><span data-stu-id="337ca-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="337ca-113">Créez une application COM+ vide.</span><span class="sxs-lookup"><span data-stu-id="337ca-113">Create an empty COM+ application.</span></span> <span data-ttu-id="337ca-114">Pour obtenir des instructions sur la procédure à suivre, consultez [création d’une application com+](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="337ca-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="337ca-115">Installez la bibliothèque de classes que vous avez créée dans l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="337ca-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="337ca-116">Pour obtenir des instructions sur la procédure à suivre, consultez [installation de nouveaux composants](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="337ca-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="337ca-117">Dans l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ que vous avez créée, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="337ca-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="337ca-118">Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="337ca-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="337ca-119">Assurez-vous que le **type d’activation** est défini sur **application serveur**.</span><span class="sxs-lookup"><span data-stu-id="337ca-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="337ca-120">Dans la zone de texte **répertoire racine** de l’application, entrez le chemin d’accès ou accédez au répertoire dans lequel vous souhaitez stocker vos fichiers de configuration d’application pour cette application.</span><span class="sxs-lookup"><span data-stu-id="337ca-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="337ca-121">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="337ca-121">Click **OK**.</span></span>

    <span data-ttu-id="337ca-122">Notez que vous pouvez également spécifier le répertoire racine de l’application COM+ à l’aide de la propriété ApplicationDirectory de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="337ca-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="337ca-123">Pour plus d’informations, consultez [**applications**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="337ca-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="337ca-124">Dans le répertoire que vous avez choisi pour stocker vos fichiers de configuration d’application, créez un fichier nommé *application*. manifest.</span><span class="sxs-lookup"><span data-stu-id="337ca-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="337ca-125">Avec un éditeur de texte, ajoutez le texte suivant à ce fichier :</span><span class="sxs-lookup"><span data-stu-id="337ca-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="337ca-126">Dans le même répertoire, créez un fichier nommé *application*. config. Avec un éditeur de texte, ajoutez le texte suivant à ce fichier :</span><span class="sxs-lookup"><span data-stu-id="337ca-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="337ca-127">Notez que ce fichier de configuration n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="337ca-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="337ca-128">Vous pouvez créer plusieurs clés avec des noms et des valeurs différents.</span><span class="sxs-lookup"><span data-stu-id="337ca-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="337ca-129">Notez, toutefois, que « ConfigData1 » correspond au nom de paramètre utilisé dans la bibliothèque de classes créée précédemment.</span><span class="sxs-lookup"><span data-stu-id="337ca-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="337ca-130">Créez une application console .NET, avec une référence à la bibliothèque de classes .NET que vous avez créée précédemment et une référence à l’assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="337ca-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="337ca-131">L’application console doit contenir le code suivant :</span><span class="sxs-lookup"><span data-stu-id="337ca-131">The console application should contain the following code:</span></span>
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

    

<span data-ttu-id="337ca-132">Exécutez l’application console.</span><span class="sxs-lookup"><span data-stu-id="337ca-132">Run the console application.</span></span> <span data-ttu-id="337ca-133">La sortie doit être :</span><span class="sxs-lookup"><span data-stu-id="337ca-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



