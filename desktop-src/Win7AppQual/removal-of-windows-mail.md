---
description: Suppression de Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Suppression de Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116277"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="1c44c-103">Suppression de Windows Mail</span><span class="sxs-lookup"><span data-stu-id="1c44c-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="1c44c-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="1c44c-104">Affected Platforms</span></span>

<span data-ttu-id="1c44c-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c44c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1c44c-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c44c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1c44c-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1c44c-107">Feature Impact</span></span>

<span data-ttu-id="1c44c-108">**Gravité** -haute</span><span class="sxs-lookup"><span data-stu-id="1c44c-108">**Severity** - High</span></span>  
<span data-ttu-id="1c44c-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="1c44c-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="1c44c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1c44c-110">Description</span></span>

<span data-ttu-id="1c44c-111">Microsoft déprécie l’utilitaire de messagerie Windows et désactive l’API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="1c44c-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="1c44c-112">Les autres API de messagerie ont été marquées comme dépréciées et sont susceptibles d’être supprimées dans une version ultérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c44c-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="1c44c-113">Toutefois, les API documentées publiquement qui ne sont pas marquées comme dépréciées ou obsolètes continuent de fonctionner dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c44c-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="1c44c-114">Les binaires restent sur les systèmes des utilisateurs et continuent à être accessibles via les API, en particulier dans les cas mentionnés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1c44c-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="1c44c-115">En outre, les fichiers de courrier électronique (. eml) et les fichiers de News (. NWS) des utilisateurs resteront sur le système.</span><span class="sxs-lookup"><span data-stu-id="1c44c-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="1c44c-116">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="1c44c-116">Manifestation of Impact</span></span>

<span data-ttu-id="1c44c-117">La suppression des résultats Windows Mail est due à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1c44c-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="1c44c-118">Tous les points d’entrée vers Windows Mail et contacts (par exemple, le menu Démarrer, les raccourcis créés par l’utilisateur, l’exécution de démarrage >, etc.) sont supprimés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="1c44c-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="1c44c-119">Certaines d’entre elles sont complètement supprimées, d’autres échouent lors de la tentative de lancement.</span><span class="sxs-lookup"><span data-stu-id="1c44c-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="1c44c-120">Toutes les dll sont expédiées dans la zone</span><span class="sxs-lookup"><span data-stu-id="1c44c-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="1c44c-121">Les API documentées publiquement continuent de fonctionner comme dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c44c-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="1c44c-122">Toutes les API qui tentent de lancer l’interface utilisateur principale du navigateur ont été modifiées pour créer une défaillance silencieuse.</span><span class="sxs-lookup"><span data-stu-id="1c44c-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="1c44c-123">La fonction retourne Success, mais n’affiche pas l’interface utilisateur pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c44c-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="1c44c-124">Les API qui appellent d’autres boîtes de dialogue (par exemple, le spouleur ou la boîte de dialogue comptes) continuent à afficher cette interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c44c-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="1c44c-125">Les gestionnaires de protocole (mailto, LDAP, News, SNEWS, NNTP) ne sont pas associés à Windows Mail ou aux contacts.</span><span class="sxs-lookup"><span data-stu-id="1c44c-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="1c44c-126">Lorsque vous tentez de les lancer, les clients voient une boîte de dialogue d’erreur qui les pointe vers l’emplacement où ils peuvent définir ces associations sur un autre programme.</span><span class="sxs-lookup"><span data-stu-id="1c44c-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="1c44c-127">Les associations de fichiers (. eml,. NWS,. contact,. Group,. wab,. P7C,. VFC) sont interrompues ou désactivées.</span><span class="sxs-lookup"><span data-stu-id="1c44c-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="1c44c-128">Lorsque vous tentez d’ouvrir un fichier avec ces extensions, les clients obtiennent une boîte de dialogue leur proposant d’autres applications installées qu’ils peuvent utiliser et les pointant vers une page Web proposant des solutions</span><span class="sxs-lookup"><span data-stu-id="1c44c-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="1c44c-129">Tout fichier utilisateur (par exemple, les fichiers ou les messages de contact) reste sur le système dans le scénario de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="1c44c-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="1c44c-130">Le dossier contacts est masqué par défaut afin que les clients ne le voient pas</span><span class="sxs-lookup"><span data-stu-id="1c44c-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="1c44c-131">Les API sont marquées comme dépréciées dans MSDN</span><span class="sxs-lookup"><span data-stu-id="1c44c-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="1c44c-132">La fonction d’aperçu de fichier est supprimée</span><span class="sxs-lookup"><span data-stu-id="1c44c-132">The file preview function is removed</span></span>
-   <span data-ttu-id="1c44c-133">Les hooks de l’interpréteur de commandes dans le menu contextuel sont supprimés</span><span class="sxs-lookup"><span data-stu-id="1c44c-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="1c44c-134">La fonction de recherche de fichiers est supprimée</span><span class="sxs-lookup"><span data-stu-id="1c44c-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="1c44c-135">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="1c44c-135">Mitigation</span></span>

<span data-ttu-id="1c44c-136">Les utilisateurs doivent installer Windows Live Mail ou tout autre produit de messagerie capable de lire les fichiers. eml et. NWS.</span><span class="sxs-lookup"><span data-stu-id="1c44c-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="1c44c-137">Solution</span><span class="sxs-lookup"><span data-stu-id="1c44c-137">Solution</span></span>

<span data-ttu-id="1c44c-138">Détecte si un gestionnaire de messagerie par défaut est installé.</span><span class="sxs-lookup"><span data-stu-id="1c44c-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="1c44c-139">Si ce n’est pas le cas, conseillez à l’utilisateur d’installer Windows Live Mail ou tout autre produit capable de lire les fichiers. eml et. NWS.</span><span class="sxs-lookup"><span data-stu-id="1c44c-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="1c44c-140">Ne concevez pas le code qui appelle l’API d’interface utilisateur de Windows Mail, car il ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="1c44c-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="1c44c-141">Vous devez trouver d’autres façons d’accéder aux fichiers. eml et. NWS.</span><span class="sxs-lookup"><span data-stu-id="1c44c-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="1c44c-142">En outre, dès que possible, interrompez votre confiance sur toutes les autres API Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="1c44c-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="1c44c-143">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="1c44c-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="1c44c-144">Exercez votre application dans un environnement Windows 7 pour vous assurer que l’application n’essaie pas d’appeler l’API d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c44c-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="1c44c-145">Vous pouvez également exécuter Application Compatibility Toolkit (ACT) à l’aide de l’évaluateur de compatibilité Windows (WCE) pour localiser les problèmes potentiels en raison de l’obsolescence de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1c44c-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1c44c-146">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="1c44c-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="1c44c-147">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="1c44c-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
