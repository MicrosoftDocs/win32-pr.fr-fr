---
description: Windows Installer accepte une Uniform Resource Locator (URL) comme source valide pour une installation.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Téléchargement d’une installation à partir d’Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527373"
---
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="cf39c-103">Téléchargement d’une installation à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="cf39c-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="cf39c-104">Windows Installer accepte une Uniform Resource Locator (URL) comme source valide pour une installation.</span><span class="sxs-lookup"><span data-stu-id="cf39c-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="cf39c-105">Windows Installer pouvez installer des packages, des correctifs et des transformations à partir d’un emplacement d’URL.</span><span class="sxs-lookup"><span data-stu-id="cf39c-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="cf39c-106">Si la base de données d’installation se trouve sur une URL, le programme d’installation télécharge la base de données dans un emplacement de cache avant de commencer l’installation.</span><span class="sxs-lookup"><span data-stu-id="cf39c-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="cf39c-107">Le programme d’installation télécharge également les fichiers et fichiers CAB à partir de la source Internet qui sont appropriés pour les sélections de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf39c-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="cf39c-108">Pour plus d’informations, consultez [un exemple d’installation de Windows Installer basé sur une URL](a-url-based-windows-installer-installation-example.md) .</span><span class="sxs-lookup"><span data-stu-id="cf39c-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="cf39c-109">Par exemple, pour installer un package avec une source située sur un serveur Web à https://server/share/package.msi l’adresse, vous pouvez utiliser les options de [ligne de commande](command-line-options.md) pour installer le package et définir des propriétés [publiques](public-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="cf39c-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="cf39c-110">msiexec/i https://server/share/package.msi *Property = value*</span><span class="sxs-lookup"><span data-stu-id="cf39c-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="cf39c-111">Une ligne de commande semblable à celle présentée précédemment doit être passée au programme d’installation pour démarrer une installation à partir d’un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="cf39c-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="cf39c-112">En général, vous ne devez pas télécharger et installer le package simplement en double-cliquant sur le fichier. msi à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf39c-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="cf39c-113">Cela permet de télécharger le fichier. msi dans le dossier Temporary Internet Files et de transmettre la commande suivante au programme d’installation :</span><span class="sxs-lookup"><span data-stu-id="cf39c-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="cf39c-114">**msiexec/i c : \\ \\ fichiers Internet temporaires Windows \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="cf39c-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="cf39c-115">L’installation échoue si le package nécessite des fichiers sources externes ou des armoires, car ceux-ci ne se trouvent pas au même emplacement que le fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="cf39c-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="cf39c-116">Notez que, étant donné que l’objet [**installer**](installer-object.md) n’est pas marqué comme [SafeForScripting](safeforscripting.md) sur l’ordinateur de l’utilisateur, les utilisateurs doivent ajuster les paramètres de sécurité de leur navigateur pour que l’exemple fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cf39c-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="cf39c-117">La méthode [**InstallProduct**](installer-installproduct.md) peut être utilisée pour exécuter la commande précédente à partir d’un navigateur en tant qu’événement de clic.</span><span class="sxs-lookup"><span data-stu-id="cf39c-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="cf39c-118">Notez que, étant donné que certains serveurs Web respectent la casse, le champ de nom de fichier dans la table de [fichiers](file-table.md) doit correspondre exactement à la casse des fichiers sources pour garantir la prise en charge des téléchargements Internet.</span><span class="sxs-lookup"><span data-stu-id="cf39c-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="cf39c-119">Consultez [téléchargement et installation d’un correctif à partir d’Internet](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="cf39c-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="cf39c-120">Pour plus d’informations sur la sécurisation des installations et l’utilisation des certificats numériques, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [signatures numériques et de Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="cf39c-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="cf39c-121">Pour plus d’informations sur la création d’une installation Web d’un package de Windows Installer, consultez [démarrage du téléchargement sur Internet](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="cf39c-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="cf39c-122">Protocoles Internet disponibles</span><span class="sxs-lookup"><span data-stu-id="cf39c-122">Available Internet Protocols</span></span>

<span data-ttu-id="cf39c-123">À compter de Windows Server 2003 et Windows XP, le programme d’installation peut utiliser les protocoles HTTP, HTTPs et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cf39c-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="cf39c-124">Le programme d’installation ne prend pas en charge les protocoles FTP et GOPHER.</span><span class="sxs-lookup"><span data-stu-id="cf39c-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="cf39c-125">Windows Installer version 2,0 peut utiliser les protocoles HTTP, fichier et FTP et ne peut pas utiliser les protocoles HTTPs et GOPHER.</span><span class="sxs-lookup"><span data-stu-id="cf39c-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



