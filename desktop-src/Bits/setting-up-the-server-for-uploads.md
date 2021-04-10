---
title: Configuration du serveur pour les téléchargements
description: Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur. Pour connaître la configuration requise pour IIS, consultez configuration IIS requise pour les téléchargements BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190795"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="4db89-104">Configuration du serveur pour les téléchargements</span><span class="sxs-lookup"><span data-stu-id="4db89-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="4db89-105">Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4db89-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="4db89-106">Pour connaître la configuration requise pour IIS, consultez [configuration IIS requise pour les téléchargements bits](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="4db89-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="4db89-107">Pour plus d’informations sur la configuration du répertoire virtuel IIS utilisé par BITS pour les téléchargements, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="4db89-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="4db89-108">Définition des autorisations sur les répertoires virtuels</span><span class="sxs-lookup"><span data-stu-id="4db89-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="4db89-109">Écriture d’un script pour configurer le répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="4db89-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="4db89-110">Utilisation de l’interface utilisateur IIS pour configurer le répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="4db89-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="4db89-111">Empêcher plusieurs chargements</span><span class="sxs-lookup"><span data-stu-id="4db89-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="4db89-112">Télécharger les meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="4db89-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="4db89-113">Certaines installations IIS incluent le composant de filtrage UrlScan.</span><span class="sxs-lookup"><span data-stu-id="4db89-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="4db89-114">Si UrlScan est activé, l’administrateur doit ajouter le verbe « BITS \_ auto » à la liste des verbes HTTP autorisés d’URLScan.</span><span class="sxs-lookup"><span data-stu-id="4db89-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="4db89-115">Dans le cas contraire, les téléchargements du client BITS échoueront.</span><span class="sxs-lookup"><span data-stu-id="4db89-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="4db89-116">Pour plus d’informations sur l’activation des verbes dans UrlScan, consultez la documentation d’UrlScan.</span><span class="sxs-lookup"><span data-stu-id="4db89-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




