---
title: Installation du fournisseur
description: La procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, fournisseur WMI, installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671965"
---
# <a name="installing-the-provider"></a><span data-ttu-id="013d8-104">Installation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="013d8-104">Installing the Provider</span></span>

<span data-ttu-id="013d8-105">La procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé.</span><span class="sxs-lookup"><span data-stu-id="013d8-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="013d8-106">La procédure suivante décrit comment installer et configurer le fournisseur WMI DNS sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="013d8-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="013d8-107">Pour obtenir le fournisseur WMI DNS pour Windows 2000, téléchargez le fichier suivant :</span><span class="sxs-lookup"><span data-stu-id="013d8-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="013d8-108">**Avertissement :** Les fichiers de fournisseur WMI DNS ne sont pas interchangeables.</span><span class="sxs-lookup"><span data-stu-id="013d8-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="013d8-109">Les serveurs DNS Windows 2000 requièrent des fichiers différents et une procédure différente des serveurs DNS Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="013d8-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="013d8-110">La procédure pour chaque est fournie.</span><span class="sxs-lookup"><span data-stu-id="013d8-110">The procedure for each is provided.</span></span>

<span data-ttu-id="013d8-111">**Pour installer le fournisseur WMI DNS sur le serveur Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="013d8-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="013d8-112">Procurez-vous le fournisseur WMI DNS pour Windows 2000 à partir du kit de ressources du serveur Windows 2000, ou téléchargez le fichier, Dnsprov.zip, à partir de : ftp://ftp.microsoft.com/reskit/win2000/</span><span class="sxs-lookup"><span data-stu-id="013d8-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="013d8-113">Copiez les fichiers du fournisseur WMI DNS (Dnsprov.dll) et Dnsschema. mof dans le <winntdir> \\ \\ répertoire system32 wbem.</span><span class="sxs-lookup"><span data-stu-id="013d8-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="013d8-114">Compilez le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="013d8-114">Compile the MOF file.</span></span> <span data-ttu-id="013d8-115">Cela permet de personnaliser le schéma pour qu’il corresponde au serveur.</span><span class="sxs-lookup"><span data-stu-id="013d8-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="013d8-116">**mofcomp Dnsschema. mof**</span><span class="sxs-lookup"><span data-stu-id="013d8-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="013d8-117">Inscrivez la DLL sur le serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="013d8-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="013d8-118">**dnsprov.dllregsvr32**</span><span class="sxs-lookup"><span data-stu-id="013d8-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="013d8-119">Les scripts ou les programmes qui utilisent le fournisseur WMI DNS pour gérer les serveurs DNS peuvent ensuite être utilisés.</span><span class="sxs-lookup"><span data-stu-id="013d8-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="013d8-120">Les scripts ou les programmes peuvent être exécutés à partir du serveur DNS ou à partir d’un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="013d8-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="013d8-121">Le kit de développement logiciel (SDK) WMI n’est pas requis pour exécuter le fournisseur WMI DNS, mais il contient de nombreux outils utiles.</span><span class="sxs-lookup"><span data-stu-id="013d8-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="013d8-122">Le fournisseur WMI DNS doit être installé sur n’importe quel serveur DNS à gérer ; Toutefois, les scripts DNS peuvent être exécutés sur le serveur DNS ou sur un hôte distant.</span><span class="sxs-lookup"><span data-stu-id="013d8-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="013d8-123">**Pour installer le fournisseur WMI DNS sur Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="013d8-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="013d8-124">Pour les systèmes d’exploitation Windows Server 2003, le fournisseur WMI DNS est automatiquement installé et inscrit, et son fichier MOF est compilé lors de l’installation du service serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="013d8-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




