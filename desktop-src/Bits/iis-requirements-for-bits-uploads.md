---
title: Configuration requise pour IIS pour les téléchargements BITS
description: Pour les téléchargements, BITS requiert IIS 6,0 sur Windows Server 2003 et IIS 7,0 sur Windows Server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671613"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="254b9-103">Configuration requise pour IIS pour les téléchargements BITS</span><span class="sxs-lookup"><span data-stu-id="254b9-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="254b9-104">Pour les téléchargements, BITS requiert IIS 6,0 sur Windows Server 2003 et IIS 7,0 sur Windows Server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="254b9-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="254b9-105">Le répertoire virtuel IIS doit être activé pour les téléchargements et les extensions IIS BITS doivent être configurées.</span><span class="sxs-lookup"><span data-stu-id="254b9-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="254b9-106">**Installations principales de Windows Server :** Les extensions IIS BITS ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="254b9-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="254b9-107">Sur Windows Server 2008, utilisez la **Gestionnaire de serveur** pour installer la fonctionnalité extensions du serveur bits.</span><span class="sxs-lookup"><span data-stu-id="254b9-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="254b9-108">Dans **Gestionnaire de serveur**, cliquez sur **fonctionnalités** dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="254b9-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="254b9-109">Dans l' **Assistant Ajout de fonctionnalités**, activez les extensions du serveur bits.</span><span class="sxs-lookup"><span data-stu-id="254b9-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="254b9-110">Notez que les rôles de compatibilité avec la gestion IIS 6 doivent être installés.</span><span class="sxs-lookup"><span data-stu-id="254b9-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="254b9-111">Sur Windows Server 2003, utilisez l' **Assistant Composants Windows** pour installer l’extension de serveur bits.</span><span class="sxs-lookup"><span data-stu-id="254b9-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="254b9-112">Dans **le panneau de configuration**, sélectionnez **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="254b9-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="254b9-113">Ensuite, sélectionnez **Ajouter/supprimer des composants Windows** pour afficher l **'Assistant composants de Windows**.</span><span class="sxs-lookup"><span data-stu-id="254b9-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="254b9-114">L’extension du serveur BITS est un sous-composant de Internet Information Services (IIS) qui est un sous-composant du serveur d’applications Web.</span><span class="sxs-lookup"><span data-stu-id="254b9-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="254b9-115">Si le service IISAdmin est redémarré, le processus de travail IIS doit être recyclé pour que le service BITS puisse reprendre les téléchargements.</span><span class="sxs-lookup"><span data-stu-id="254b9-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="254b9-116">Le processus de travail IIS peut être recyclé manuellement à l’aide de l’utilitaire de ligne de commande **IISReset.exe** .</span><span class="sxs-lookup"><span data-stu-id="254b9-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="254b9-117">Pour plus d’informations sur la configuration d’IIS pour les chargements, consultez [configuration du serveur pour les téléchargements](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="254b9-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="254b9-118">Pour plus d’informations sur les propriétés que BITS ajoute à IIS, consultez [paramètres du serveur bits pour les travaux de téléchargement](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="254b9-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




