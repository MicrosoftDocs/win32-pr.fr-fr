---
title: Journalisation du client (kit de développement logiciel (SDK) Windows Media format 11)
description: Journalisation du client
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, journalisation du client
- Windows Media Format SDK, journalisation
- ASF (Advanced Systems Format), journalisation du client
- ASF (format des systèmes avancés), journalisation du client
- ASF (Advanced Systems Format), journalisation
- ASF (format des systèmes avancés), journalisation
- journalisation du client
- journalisation des clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102629"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="f484e-111">Journalisation du client (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="f484e-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f484e-112">Lorsque l’objet lecteur lit les données à partir d’un serveur, il envoie les informations de journalisation au serveur.</span><span class="sxs-lookup"><span data-stu-id="f484e-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="f484e-113">Les fournisseurs de contenu utilisent généralement ces informations pour mesurer la qualité de service, générer des informations de facturation ou suivre la publicité.</span><span class="sxs-lookup"><span data-stu-id="f484e-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="f484e-114">Les informations de journalisation ne contiennent aucune donnée personnelle.</span><span class="sxs-lookup"><span data-stu-id="f484e-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="f484e-115">L’application peut spécifier certaines des informations qui sont journalisées, en appelant la méthode [**IWMReaderAdvanced :: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="f484e-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="f484e-116">Par exemple, vous pouvez spécifier la chaîne User-agent, le nom de l’application Player ou la page Web qui héberge le lecteur.</span><span class="sxs-lookup"><span data-stu-id="f484e-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="f484e-117">Les informations de journalisation incluent un GUID qui identifie la session.</span><span class="sxs-lookup"><span data-stu-id="f484e-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="f484e-118">Par défaut, le lecteur génère un ID de session anonyme.</span><span class="sxs-lookup"><span data-stu-id="f484e-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="f484e-119">Le lecteur peut éventuellement envoyer un ID qui identifie de façon unique l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f484e-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="f484e-120">Pour activer cette fonctionnalité, appelez la méthode [**IWMReaderAdvanced2 :: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="f484e-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="f484e-121">Vous pouvez configurer l’objet lecteur pour envoyer les informations de journalisation à un autre serveur, en plus du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="f484e-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="f484e-122">Pour ce faire, appelez la méthode [**IWMReaderNetworkConfig :: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) avec l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="f484e-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="f484e-123">Cette URL doit pointer vers un script ou un exécutable qui peut gérer les requêtes HTTP et de publication.</span><span class="sxs-lookup"><span data-stu-id="f484e-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="f484e-124">Vous pouvez utiliser l’agent de publication de la multidiffusion et de la journalisation (wmsiislog.dll), ou vous pouvez écrire un script ASP ou CGI personnalisé pour recevoir les données du journal.</span><span class="sxs-lookup"><span data-stu-id="f484e-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="f484e-125">Vous pouvez obtenir la même fonctionnalité en créant une sélection côté serveur avec un attribut **logURL** .</span><span class="sxs-lookup"><span data-stu-id="f484e-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="f484e-126">Lorsque l’objet lecteur envoie le journal, il effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f484e-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="f484e-127">Envoie une requête d’extraction vide au serveur.</span><span class="sxs-lookup"><span data-stu-id="f484e-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="f484e-128">Analyse la réponse du serveur pour l’une des chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f484e-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="f484e-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` où « 0.0.0.0 » correspond à un numéro de version valide.</span><span class="sxs-lookup"><span data-stu-id="f484e-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="f484e-130">Envoie une demande de publication avec les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="f484e-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="f484e-131">Le code suivant montre un exemple de script ASP qui reçoit les informations de journalisation et les écrit dans un fichier :</span><span class="sxs-lookup"><span data-stu-id="f484e-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="f484e-132">Vous pouvez spécifier plusieurs serveurs pour recevoir les informations de journalisation ; il vous suffit d’appeler **AddLoggingUrl** une fois avec chaque URL.</span><span class="sxs-lookup"><span data-stu-id="f484e-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="f484e-133">Pour effacer la liste des serveurs qui reçoivent des journaux, appelez la méthode [**IWMReaderNetworkConfig :: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .</span><span class="sxs-lookup"><span data-stu-id="f484e-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f484e-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f484e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f484e-135">**Implémentation des fonctionnalités réseau**</span><span class="sxs-lookup"><span data-stu-id="f484e-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="f484e-136">**Interface IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="f484e-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="f484e-137">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="f484e-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




