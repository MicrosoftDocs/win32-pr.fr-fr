---
title: Authentification (kit de développement logiciel (SDK) Windows Media format 11)
description: Authentification
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, authentification
- Windows Media Format SDK, authentification réseau
- ASF (Advanced Systems Format), authentification
- ASF (format des systèmes avancés), authentification
- ASF (Advanced Systems Format), authentification réseau
- ASF (format des systèmes avancés), authentification réseau
- Authentification
- authentification réseau, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512137"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="a2007-111">Authentification (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="a2007-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a2007-112">L’objet lecteur peut gérer les défis liés à l’authentification réseau, y compris l’authentification Digest et l’authentification NTLM.</span><span class="sxs-lookup"><span data-stu-id="a2007-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="a2007-113">Dans certains cas, l’application doit fournir les informations d’identification de l’utilisateur par le biais d’une interface de rappel :</span><span class="sxs-lookup"><span data-stu-id="a2007-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="a2007-114">Authentification Digest : l’application doit implémenter l’interface **IWMCredentialCallback** , comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a2007-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="a2007-115">Authentification NTLM : le lecteur répond automatiquement avec les informations d’identification d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2007-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="a2007-116">Si l’utilisateur actuel est autorisé à se connecter au serveur, l’application n’a rien à faire.</span><span class="sxs-lookup"><span data-stu-id="a2007-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="a2007-117">Si l’utilisateur n’a pas d’autorisation, l’application doit implémenter l’interface **IWMCredentialCallback** .</span><span class="sxs-lookup"><span data-stu-id="a2007-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="a2007-118">Windows Media Services version 4,1 ne prend pas en charge l’authentification NTLM par le biais d’un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="a2007-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="a2007-119">L’authentification NTLM requiert plusieurs échanges client-serveur sur la même connexion, et la version 4,1 ne conserve pas de connexion permanente avec le proxy.</span><span class="sxs-lookup"><span data-stu-id="a2007-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="a2007-120">Windows Media Services 9 Series dans Microsoft Windows Server 2003 prend en charge l’authentification NTLM via un serveur proxy, à condition que le proxy prenne en charge les connexions persistantes.</span><span class="sxs-lookup"><span data-stu-id="a2007-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="a2007-121">Comme indiqué, dans certains cas, l’application doit fournir les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2007-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="a2007-122">Cela se produit par le biais de l’interface **IWMCredentialCallback** , qui a une méthode unique, **AcquireCredentials**.</span><span class="sxs-lookup"><span data-stu-id="a2007-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="a2007-123">Pour prendre en charge l’authentification, implémentez cette interface dans votre application.</span><span class="sxs-lookup"><span data-stu-id="a2007-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="a2007-124">L’objet lecteur interroge cette interface en appelant **QueryInterface** sur le pointeur [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) qu’il a reçu de l’application dans la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="a2007-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="a2007-125">Si l’objet lecteur doit recevoir les informations d’identification de l’utilisateur, il appelle la méthode **AcquireCredentials** de l’application.</span><span class="sxs-lookup"><span data-stu-id="a2007-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="a2007-126">Si les informations d’identification sont envoyées sur le réseau sans chiffrement, le lecteur définit l' \_ \_ \_ indicateur de texte en clair des informations d’identification WMT dans le paramètre *pdwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a2007-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="a2007-127">Cela donne à l’application la possibilité d’avertir l’utilisateur que ses informations d’identification seront envoyées en texte brut.</span><span class="sxs-lookup"><span data-stu-id="a2007-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="a2007-128">Dans le cas contraire, l’objet lecteur chiffre automatiquement les informations d’identification avant de les envoyer sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="a2007-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="a2007-129">L’application peut les retourner à l’objet lecteur en texte brut.</span><span class="sxs-lookup"><span data-stu-id="a2007-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="a2007-130">En outre, si l’objet lecteur définit l' \_ indicateur de chiffrement des informations d’identification WMT \_ , le lecteur prend en charge l’obtention d’informations d’identification chiffrées à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="a2007-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="a2007-131">Dans ce cas, l’application peut soit retourner les informations d’identification en texte brut, soit les chiffrer elle-même à l’aide de la fonction **CryptProtectData** , qui est décrite dans la documentation du kit de développement logiciel (SDK) Platform.</span><span class="sxs-lookup"><span data-stu-id="a2007-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="a2007-132">Si l’application chiffre les informations d’identification, elle doit définir l' \_ \_ indicateur de chiffrement des informations d’identification WMT dans le paramètre *pdwFlags* avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a2007-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="a2007-133">En règle générale, il n’est pas nécessaire de chiffrer les données, car l’objet lecteur chiffre les données si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a2007-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="a2007-134">Toutefois, le chiffrement peut être utile si l’application conserve le nom d’utilisateur et le mot de passe en mémoire, car elle empêche une personne malveillante d’inspecter une image mémoire du processus.</span><span class="sxs-lookup"><span data-stu-id="a2007-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2007-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2007-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2007-136">**Interface IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="a2007-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="a2007-137">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="a2007-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




