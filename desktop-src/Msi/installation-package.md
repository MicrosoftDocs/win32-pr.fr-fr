---
description: Un package d’installation contient toutes les informations dont l’Windows Installer a besoin pour installer ou désinstaller une application ou un produit et pour exécuter l’interface utilisateur du programme d’installation.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Package d'installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534573"
---
# <a name="installation-package"></a><span data-ttu-id="ff36a-103">Package d'installation</span><span class="sxs-lookup"><span data-stu-id="ff36a-103">Installation Package</span></span>

<span data-ttu-id="ff36a-104">Un package d’installation contient toutes les informations dont l’Windows Installer a besoin pour installer ou désinstaller une application ou un produit et pour exécuter l’interface utilisateur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="ff36a-105">Chaque package d’installation comprend un fichier. msi, contenant une base de données d’installation, un flux d’informations de synthèse et des flux de données pour différentes parties de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="ff36a-106">Le fichier. msi peut également contenir une ou plusieurs transformations, des fichiers sources internes, des fichiers sources externes ou des fichiers CAB requis par l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="ff36a-107">Les développeurs d’applications doivent créer une installation pour utiliser le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="ff36a-108">Étant donné que le programme d’installation organise les installations autour du concept de [composants et de fonctionnalités](components-and-features.md), et stocke toutes les informations relatives à l’installation dans une base de données relationnelle, le processus de création d’un package d’installation implique une large part des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff36a-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="ff36a-109">Identifiez les fonctionnalités à présenter aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff36a-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="ff36a-110">Organisez l’application en composants.</span><span class="sxs-lookup"><span data-stu-id="ff36a-110">Organize the application into components.</span></span>
-   <span data-ttu-id="ff36a-111">Remplissez la base de données d’installation avec les informations.</span><span class="sxs-lookup"><span data-stu-id="ff36a-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="ff36a-112">Validez le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-112">Validate the installation package.</span></span>

<span data-ttu-id="ff36a-113">La section suivante décrit les composants et les fonctionnalités du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="ff36a-114">Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="ff36a-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="ff36a-115">Le choix des fonctionnalités est généralement déterminé par les fonctionnalités de l’application du point de vue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff36a-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="ff36a-116">Il est recommandé que les développeurs utilisent une procédure standard pour choisir des composants.</span><span class="sxs-lookup"><span data-stu-id="ff36a-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="ff36a-117">Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="ff36a-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="ff36a-118">Les auteurs de package peuvent utiliser des outils de création de packages tiers, ou un éditeur de table et le kit de développement logiciel (SDK) Windows Installer, pour remplir la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff36a-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="ff36a-119">Tous les packages d’installation doivent être validés pour assurer la cohérence interne.</span><span class="sxs-lookup"><span data-stu-id="ff36a-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="ff36a-120">Pour plus d’informations, consultez [validation de package](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="ff36a-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



