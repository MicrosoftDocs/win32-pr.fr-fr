---
description: Les journaux WinHTTP peuvent être utilisés pour aider à résoudre les problèmes liés aux applications WSDAPI. Cela est utile lorsque l’échange de métadonnées échoue ou lorsque la négociation SSL/TLS échoue.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Capture des journaux WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115027"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="75e39-104">Capture des journaux WinHTTP</span><span class="sxs-lookup"><span data-stu-id="75e39-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="75e39-105">Les journaux [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) peuvent être utilisés pour aider à résoudre les problèmes liés aux applications wsdapi.</span><span class="sxs-lookup"><span data-stu-id="75e39-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="75e39-106">Cela est utile lorsque l’échange de métadonnées échoue ou lorsque la négociation SSL/TLS échoue.</span><span class="sxs-lookup"><span data-stu-id="75e39-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="75e39-107">Cette procédure montre comment capturer des journaux WinHTTP sur le PC client.</span><span class="sxs-lookup"><span data-stu-id="75e39-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="75e39-108">L’application cliente WSDAPI ne doit pas être en cours d’exécution lorsque la journalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="75e39-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="75e39-109">Si l’application cliente est en cours d’exécution lorsque la journalisation est activée, le client et/ou le PC doivent être redémarrés pour que les WS-Discovery et le trafic d’échange de métadonnées s’affichent dans les journaux WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="75e39-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="75e39-110">**Pour capturer les journaux WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="75e39-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="75e39-111">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges sur le PC client.</span><span class="sxs-lookup"><span data-stu-id="75e39-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="75e39-112">Exécutez la commande suivante : **netsh WinHTTP Set Tracing trace-file-prefix = "C : \\ temp \\ DPWS" niveau = verbose format = ANSI State = Enabled Max-trace-file-Size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="75e39-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="75e39-113">Cette commande active la journalisation WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="75e39-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="75e39-114">Tous les fichiers journaux sont stockés dans le répertoire C : \\ temp, et les noms de fichiers commencent par le préfixe DPWS.</span><span class="sxs-lookup"><span data-stu-id="75e39-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="75e39-115">Au plus 1 Go de fichiers journaux seront stockés.</span><span class="sxs-lookup"><span data-stu-id="75e39-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="75e39-116">Si le processus utilisant WinHTTP sur le client est déjà en cours d’exécution, redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="75e39-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="75e39-117">Par exemple, si les API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) sont utilisées, l’ordinateur doit être redémarré.</span><span class="sxs-lookup"><span data-stu-id="75e39-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="75e39-118">Les API de détection de fonction appellent WinHTTP depuis l’intérieur d’un hôte de service, qui a peut-être déjà démarré lorsque le suivi a été activé.</span><span class="sxs-lookup"><span data-stu-id="75e39-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="75e39-119">Démarrez l’application cliente WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="75e39-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="75e39-120">L’application en cours de débogage ou le client de débogage WSD peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="75e39-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="75e39-121">Reproduire l’échec de l’application.</span><span class="sxs-lookup"><span data-stu-id="75e39-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="75e39-122">Arrêtez l’application cliente basée sur WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="75e39-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="75e39-123">Si le processus qui utilise WinHTTP n’est pas terminé avec l’application cliente, redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="75e39-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="75e39-124">Par exemple, si les API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) sont utilisées, l’ordinateur doit être redémarré.</span><span class="sxs-lookup"><span data-stu-id="75e39-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="75e39-125">Exécutez la commande suivante : **netsh WinHTTP Set Tracing State = Disabled**</span><span class="sxs-lookup"><span data-stu-id="75e39-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="75e39-126">Cette commande désactive la journalisation WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="75e39-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="75e39-127">Inspectez les journaux DPWS dans C : \\ temp et vérifiez que les demandes et les messages requis ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="75e39-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="75e39-128">Si la communication de canal sécurisé (HTTPs) est utilisée, vérifiez les défaillances SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="75e39-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="75e39-129">Une fois les journaux WinHTTP capturés, les journaux peuvent être examinés pour rechercher la cause d’un échec d’application WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="75e39-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="75e39-130">Notez que l’éditeur de texte utilisé pour afficher ces journaux doit être exécuté en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="75e39-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="75e39-131">Pour plus d’informations, consultez [utilisation de la journalisation WinHTTP pour vérifier obtenir le trafic](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="75e39-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75e39-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75e39-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75e39-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="75e39-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="75e39-134">Utilisation de la journalisation WinHTTP pour vérifier la récupération du trafic</span><span class="sxs-lookup"><span data-stu-id="75e39-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
