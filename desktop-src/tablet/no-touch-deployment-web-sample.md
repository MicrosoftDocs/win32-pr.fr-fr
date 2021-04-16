---
description: Cet exemple montre comment déployer une application Tablet PC gérée sur le Web à l’aide d’un déploiement sans toucher.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Exemple de déploiement Web No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530442"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="228f6-103">Exemple de déploiement Web No-Touch</span><span class="sxs-lookup"><span data-stu-id="228f6-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="228f6-104">Cet exemple montre comment déployer une application Tablet PC gérée sur le Web à l’aide d’un déploiement sans toucher.</span><span class="sxs-lookup"><span data-stu-id="228f6-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="228f6-105">Vous devez être familiarisé avec les concepts abordés dans [le déploiement sans toucher dans le .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span><span class="sxs-lookup"><span data-stu-id="228f6-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="228f6-106">Pour exécuter cet exemple, Microsoft Internet Information Services (IIS) doit être installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="228f6-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="228f6-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="228f6-107">Overview</span></span>

<span data-ttu-id="228f6-108">Avec le déploiement sans toucher, les applications Tablet PCWindows Forms-applications de bureau générées à l’aide des classes de l’espace de noms System. Windows. Forms de l’infrastructure Microsoft .NET et du kit de développement Microsoft Windows XP Tablet PC Edition 1,7-peuvent être téléchargées, installées et exécutées directement sur les ordinateurs des utilisateurs sans aucune modification du registre ou des composants du système partagé.</span><span class="sxs-lookup"><span data-stu-id="228f6-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="228f6-109">Cet exemple utilise le projet d’origine pour l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md), les revendications automatiques et fournit un projet de programme d’installation, \_ NoTouchWebe automatiquement.</span><span class="sxs-lookup"><span data-stu-id="228f6-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="228f6-110">Une fois compilé et exécuté, le projet d’installation crée une nouvelle racine virtuelle, également appelée \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="228f6-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="228f6-111">Le programme d’installation copie un fichier, default.htm, qui comprend un lien vers l’assembly AutoClaims.exe.</span><span class="sxs-lookup"><span data-stu-id="228f6-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="228f6-112">Pour lancer l’application cliente enrichie, accédez à la racine virtuelle avec Microsoft Internet Explorer, puis cliquez sur le lien dans la page default.htm.</span><span class="sxs-lookup"><span data-stu-id="228f6-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="228f6-113">Vous devez accéder à la racine virtuelle par le biais d’IIS (par exemple, https://localhost/AutoClaims\_NoTouchWeb/default.htm) et pas directement via le système de fichiers pour que l’application fonctionne dans le domaine d’application Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="228f6-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="228f6-114">Conditions requises pour le déploiement de No-Touch</span><span class="sxs-lookup"><span data-stu-id="228f6-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="228f6-115">Tous les assemblys dépendants doivent se trouver dans le chemin de recherche de l’assembly ou la racine du répertoire virtuel du site Web.</span><span class="sxs-lookup"><span data-stu-id="228f6-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="228f6-116">Le projet de déploiement NoTouchWeb de la récupération d' \_ origine installe l’assembly et la page de référence, default.htm, dans la même racine virtuelle (NoTouchWeb de récupération \_ ).</span><span class="sxs-lookup"><span data-stu-id="228f6-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="228f6-117">Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="228f6-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="228f6-118">Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.</span><span class="sxs-lookup"><span data-stu-id="228f6-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="228f6-119">Pour plus d’informations sur l’utilisation de l’encre sur le Web, voir [Ink on the Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="228f6-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 