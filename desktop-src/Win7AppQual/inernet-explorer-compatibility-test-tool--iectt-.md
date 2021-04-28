---
description: Outil de test de compatibilité d'Internet Explorer (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Outil de test de compatibilité d'Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088283"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="36580-103">Outil de test de compatibilité d'Internet Explorer (IECTT)</span><span class="sxs-lookup"><span data-stu-id="36580-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="36580-104">L’outil de test de compatibilité d’Internet Explorer (IECTT) est un composant de [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="36580-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="36580-105">Cet outil peut vous aider à diagnostiquer les problèmes dans vos applications Web en affichant des problèmes en temps réel et en chargeant éventuellement les résultats dans une base de données ACT.</span><span class="sxs-lookup"><span data-stu-id="36580-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="36580-106">Les résultats incluent des détails sur les problèmes de compatibilité possibles et des liens pour plus d’informations sur chaque problème de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="36580-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="36580-107">IECTT vous permet également d’exclure des problèmes et de modifier les attributs disponibles.</span><span class="sxs-lookup"><span data-stu-id="36580-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="36580-108">Pour ouvrir IECTT</span><span class="sxs-lookup"><span data-stu-id="36580-108">To open IECTT</span></span>

1.  <span data-ttu-id="36580-109">Installez [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="36580-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="36580-110">Cliquez sur **Démarrer**, pointez sur **programmes**, sur **Microsoft Application Compatibility Toolkit 5,6**, sur **outils de développement et** de test, puis cliquez sur outil de test de **compatibilité Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="36580-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="36580-111">Les sections suivantes décrivent les scénarios de IECTT courants.</span><span class="sxs-lookup"><span data-stu-id="36580-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="36580-112">Afficher les problèmes en temps réel</span><span class="sxs-lookup"><span data-stu-id="36580-112">View Issues in Real Time</span></span>

<span data-ttu-id="36580-113">Vous pouvez rechercher et afficher vos problèmes Web en temps réel, pendant que vous testez vos sites Web et applications Web sur Windows Internet Explorer 7 et Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="36580-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="36580-114">Une fois vos tests terminés, vous pouvez afficher les résultats dans l’écran de **données dynamiques** de IECTT.</span><span class="sxs-lookup"><span data-stu-id="36580-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="36580-115">Télécharger des problèmes dans votre base de données ACT</span><span class="sxs-lookup"><span data-stu-id="36580-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="36580-116">Vous pouvez télécharger vos problèmes Web dans la base de données ACT, qui traite les informations et vous permet d’afficher vos résultats sur l’écran d' **analyse** du gestionnaire de compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="36580-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="36580-117">Collecter vos données de compatibilité</span><span class="sxs-lookup"><span data-stu-id="36580-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="36580-118">Vous pouvez collecter les données de compatibilité de votre site Web et de vos applications Web à l’aide de l’outil IECTT avec Internet Explorer 7 ou Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="36580-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="36580-119">**Pour collecter vos données de compatibilité**</span><span class="sxs-lookup"><span data-stu-id="36580-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="36580-120">Fermez toutes les fenêtres actives de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36580-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="36580-121">Dans IECTT, dans la barre d’outils de l' **outil de test de compatibilité d’Internet Explorer** , cliquez sur **activer**.</span><span class="sxs-lookup"><span data-stu-id="36580-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="36580-122">Ouvrez une fenêtre Internet Explorer 7 ou Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="36580-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="36580-123">Un message s’affiche et indique que la journalisation de l’évaluation de la compatibilité est activée.</span><span class="sxs-lookup"><span data-stu-id="36580-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="36580-124">Visitez les sites Web ou les applications Web qui sont requis pour une utilisation par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="36580-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="36580-125">À mesure que vous visitez chaque site, l’outil IECTT affiche, en temps réel, vos problèmes de compatibilité potentiels.</span><span class="sxs-lookup"><span data-stu-id="36580-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="36580-126">Dans la barre d’outils de l' **outil de test de compatibilité d’Internet Explorer** , cliquez sur **Désactiver** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="36580-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="36580-127">Le processus de journalisation de compatibilité se termine et s’arrête.</span><span class="sxs-lookup"><span data-stu-id="36580-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="36580-128">Filtrer les résultats de votre problème</span><span class="sxs-lookup"><span data-stu-id="36580-128">Filter Your Issue Results</span></span>

<span data-ttu-id="36580-129">Vous pouvez filtrer tous les résultats de votre IECTT par nom d’objet, par type de problème, ou par les deux.</span><span class="sxs-lookup"><span data-stu-id="36580-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="36580-130">**Pour filtrer les résultats de votre problème**</span><span class="sxs-lookup"><span data-stu-id="36580-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="36580-131">Dans l’écran de l' **outil de test de compatibilité Internet Explorer** , cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="36580-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="36580-132">La boîte de dialogue **filtre des problèmes** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="36580-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="36580-133">Entrez le nom de l’objet que vous souhaitez afficher dans la zone **Entrez le nom de l’objet pour lequel afficher les problèmes** .</span><span class="sxs-lookup"><span data-stu-id="36580-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="36580-134">Pour plus d’informations sur cet outil et d’autres outils de développement, consultez [qu’est-ce que l’outil de test de compatibilité d’Internet Explorer ?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) dans MSDN Library et le billet [de blog sur la journalisation des applications dans IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .</span><span class="sxs-lookup"><span data-stu-id="36580-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36580-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36580-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36580-136">Outils de débogage d’applications Web et de modules complémentaires</span><span class="sxs-lookup"><span data-stu-id="36580-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
