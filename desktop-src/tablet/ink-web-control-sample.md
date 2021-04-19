---
description: Cet exemple montre comment créer un contrôle avec prise en charge de l’écriture manuscrite pour une utilisation dans un navigateur Web. L’exemple utilise l’exemple de formulaire de déclaration automatique d’origine et le transforme en un contrôle qui est placé sur une page Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Exemple de contrôle Web Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529115"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="60553-104">Exemple de contrôle Web Ink</span><span class="sxs-lookup"><span data-stu-id="60553-104">Ink Web Control Sample</span></span>

<span data-ttu-id="60553-105">Cet exemple montre comment créer un contrôle avec prise en charge de l’écriture manuscrite pour une utilisation dans un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="60553-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="60553-106">L’exemple utilise l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md) d’origine et le transforme en un contrôle qui est placé sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="60553-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="60553-107">Pour plus d’informations sur l’utilisation de l’encre sur le Web, voir [Ink on the Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="60553-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="60553-108">Modifications apportées à l’exemple de projet d’origine</span><span class="sxs-lookup"><span data-stu-id="60553-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="60553-109">Cet exemple se compose d’une solution qui inclut deux projets et un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="60553-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="60553-110">Le premier projet, réclamation, est un projet de bibliothèque de contrôles Microsoft Visual C \# (un contrôle utilisateur).</span><span class="sxs-lookup"><span data-stu-id="60553-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="60553-111">Le code source de ce contrôle est presque identique à celui de l’exemple autoclaims, à deux différences près :</span><span class="sxs-lookup"><span data-stu-id="60553-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="60553-112">`AutoClaims`Dans cet exemple, la classe hérite de la classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) et non de la classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="60553-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="60553-113">La classe autoclaims de cet exemple a une méthode publique ajoutée, `DisposeResources` qui supprime les contrôles enfants internes utilisés pour la collecte de l’encre.</span><span class="sxs-lookup"><span data-stu-id="60553-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="60553-114">Cette méthode doit être appelée par thewebpageon que le contrôle est utilisé lorsque cette page est terminée à l’aide du contrôle.</span><span class="sxs-lookup"><span data-stu-id="60553-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="60553-115">Référencement du contrôle en HTML</span><span class="sxs-lookup"><span data-stu-id="60553-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="60553-116">La solution comprend un fichier HTML, default.htm.</span><span class="sxs-lookup"><span data-stu-id="60553-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="60553-117">Ce fichier est la page vers laquelle le navigateur accède pour charger le contrôle.</span><span class="sxs-lookup"><span data-stu-id="60553-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="60553-118">Le fichier contient une <object> balise qui fait référence au contrôle.</span><span class="sxs-lookup"><span data-stu-id="60553-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="60553-119">Il comprend également un script qui est appelé lorsque la page est déchargée, comme indiqué par la présence de l’attribut OnLoad = " `OnUnload()` " dans le</span><span class="sxs-lookup"><span data-stu-id="60553-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="60553-120">balise.</span><span class="sxs-lookup"><span data-stu-id="60553-120">tag.</span></span> <span data-ttu-id="60553-121">Cette fonction appelle la `DisposeResources` méthode sur le contrôle pour s’assurer que toutes les ressources sont libérées correctement à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="60553-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="60553-122">Notez le format de la valeur de l’attribut ClassID pour la <object> balise.</span><span class="sxs-lookup"><span data-stu-id="60553-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="60553-123">Il nomme l’assembly, suivi d’un \# séparateur de signe, puis de l’espace de noms qui contient le contrôle, puis du nom de classe du contrôle.</span><span class="sxs-lookup"><span data-stu-id="60553-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="60553-124">Un contrôle utilisateur réel inclut probablement des méthodes supplémentaires utilisées pour conserver ou envoyer les données collectées dans l’application.</span><span class="sxs-lookup"><span data-stu-id="60553-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="60553-125">Le projet de contrôle d’un \_ WebControl</span><span class="sxs-lookup"><span data-stu-id="60553-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="60553-126">Le projet de contrôle de configuration de l' \_ ordinateur virtuel est un projet de déploiement qui crée un programme d’installation qui ajoute une racine virtuelle, \_ le contrôle de l’utilisateur sur le serveur Web lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="60553-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="60553-127">Le contrôle et le fichier HTML sont placés dans cette racine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="60553-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="60553-128">Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="60553-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="60553-129">Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.</span><span class="sxs-lookup"><span data-stu-id="60553-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="60553-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60553-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60553-131">Exemple de formulaire de déclaration automatique</span><span class="sxs-lookup"><span data-stu-id="60553-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="60553-132">Entrée manuscrite sur le Web</span><span class="sxs-lookup"><span data-stu-id="60553-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 
