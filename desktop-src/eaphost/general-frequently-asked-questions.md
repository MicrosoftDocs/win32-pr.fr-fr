---
title: Forum aux questions (FAQ)
description: Lisez les réponses aux questions les plus fréquemment posées sur les API EAPHost, telles que « qu’est-ce que la durée de vie d’une authentification ? ».
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106529069"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="d3ded-103">Forum aux questions (FAQ)</span><span class="sxs-lookup"><span data-stu-id="d3ded-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="d3ded-104">La rubrique suivante fournit des réponses aux questions fréquemment posées sur les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d3ded-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="d3ded-105">Forum aux questions (FAQ)</span><span class="sxs-lookup"><span data-stu-id="d3ded-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3ded-106">Question</span><span class="sxs-lookup"><span data-stu-id="d3ded-106">Question</span></span></th>
<th><span data-ttu-id="d3ded-107">Réponse</span><span class="sxs-lookup"><span data-stu-id="d3ded-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3ded-108">Qu’est-ce qu’un demandeur ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="d3ded-109">Le demandeur est l’entité à authentifier à l’aide d’EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d3ded-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="d3ded-110">Les demandeurs classiques sont les clients [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , les clients 802,3 et le service Routage et accès à distance (RRAS), clients point-à-point (PPP).</span><span class="sxs-lookup"><span data-stu-id="d3ded-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-111">Qu’est-ce qu’un homologue ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-111">What is a peer?</span></span></td>
<td><span data-ttu-id="d3ded-112">L’homologue est le côté client d’une authentification EAP.</span><span class="sxs-lookup"><span data-stu-id="d3ded-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-113">Quelle est la différence entre un homologue et un demandeur ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="d3ded-114">Le demandeur transporte les paquets, contrairement à un homologue.</span><span class="sxs-lookup"><span data-stu-id="d3ded-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="d3ded-115">Néanmoins, les termes homologue, demandeur et client sont en grande partie synonymes.</span><span class="sxs-lookup"><span data-stu-id="d3ded-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-116">Qu’est-ce qu’un authentificateur ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="d3ded-117">L’authentificateur est le point d’accès sans fil, le serveur d’accès réseau (NAS) ou le périphérique d’accès au réseau (NAD) qui authentifie le demandeur.</span><span class="sxs-lookup"><span data-stu-id="d3ded-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="d3ded-118">L’authentificateur est également appelé serveur EAP.</span><span class="sxs-lookup"><span data-stu-id="d3ded-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-119">Quelle est la durée de vie d’une authentification ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="d3ded-120">La durée de vie d’une session d’authentification unique côté client correspond à tout ce qui se produit entre les fonctions [<strong>EapHostPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) et [<strong>EapHostPeerEndSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) qui sont appelées.</span><span class="sxs-lookup"><span data-stu-id="d3ded-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="d3ded-121">La durée de vie du côté de l’authentificateur est tout ce qui se produit entre les fonctions [<strong>EapPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) et [<strong>EapPeerEndSession</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</span><span class="sxs-lookup"><span data-stu-id="d3ded-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-122">Qu’est-ce qu’un objet BLOB ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-122">What is a BLOB?</span></span> <span data-ttu-id="d3ded-123">Pourquoi convertir un objet BLOB de configuration (binaire) en XML ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="d3ded-124">Un objet BLOB est un objet binaire volumineux.</span><span class="sxs-lookup"><span data-stu-id="d3ded-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="d3ded-125">XML présente plusieurs avantages par rapport à un objet BLOB de configuration binaire.</span><span class="sxs-lookup"><span data-stu-id="d3ded-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="d3ded-126">Les données de configuration stockées dans XML sont explicites, modifiables et interplateformes.</span><span class="sxs-lookup"><span data-stu-id="d3ded-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-127">Quand dois-je convertir un objet BLOB XML stocké en objet BLOB binaire ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="d3ded-128">Il est possible de stocker un objet blob binaire ou un objet BLOB XML, mais vous devez toujours convertir l’objet BLOB XML en objet BLOB binaire avant de l’utiliser avec les API Runtime. les API Runtime ne peuvent pas accepter un répertoire XML.</span><span class="sxs-lookup"><span data-stu-id="d3ded-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-129">Que sont les méthodes natives ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-129">What are native methods?</span></span></td>
<td><span data-ttu-id="d3ded-130">Les méthodes EAP natives utilisent la nouvelle API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d3ded-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-131">Que sont les méthodes héritées ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="d3ded-132">Les méthodes EAP héritées sont définies dans la référence du protocole EAP ( [Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)).</span><span class="sxs-lookup"><span data-stu-id="d3ded-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="d3ded-133">Les méthodes EAP héritées sont disponibles pour une utilisation dans Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d3ded-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="d3ded-134">Ces méthodes peuvent ne pas être disponibles pour une utilisation dans les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d3ded-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-135">Quelle est la différence entre les méthodes héritées et natives ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="d3ded-136">Les API natives sont plus simples et ont moins de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d3ded-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="d3ded-137">Toutes les nouvelles méthodes EAP doivent être écrites à l’aide de l’API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d3ded-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-138">Qu’est-ce que la &quot; stratégie de groupe &quot; ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="d3ded-139">Pour obtenir une description de la stratégie de groupe, consultez [stratégie de groupe collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3ded-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-140">Les fonctions EAPHost peuvent-elles remplacer la stratégie de configuration spécifiée par la stratégie de groupe ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="d3ded-141">Non, jamais.</span><span class="sxs-lookup"><span data-stu-id="d3ded-141">No, never.</span></span> <span data-ttu-id="d3ded-142">Si la stratégie de groupe est en cours d’utilisation, les paramètres de stratégie de groupe remplacent toujours les paramètres de configuration EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d3ded-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-143">Qu’est-ce que l’authentification unique (SSO) ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="d3ded-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) est un mécanisme d’authentification de couche 2.</span><span class="sxs-lookup"><span data-stu-id="d3ded-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="d3ded-145">Selon la configuration de l’authentification unique, l’authentification unique permet aux utilisateurs de s’authentifier sur le réseau à l’aide de l’authentification [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) avant ou immédiatement après l’ouverture de session sur Windows.</span><span class="sxs-lookup"><span data-stu-id="d3ded-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="d3ded-146">L’authentification unique peut être configurée pour utiliser les informations d’identification Windows pour l’authentification réseau (dans ce cas, les utilisateurs entrent leurs informations d’identification une seule fois) ou utilisent des informations d’identification différentes pour l’authentification Windows et le réseau.</span><span class="sxs-lookup"><span data-stu-id="d3ded-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="d3ded-147">Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="d3ded-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-148">Qu’est-ce que le fournisseur d’accès avant ouverture de session (PLAP)</span><span class="sxs-lookup"><span data-stu-id="d3ded-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="d3ded-149">Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="d3ded-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-150">Qu’est-ce que le protocole PEAP (Protected Extensible Authentication Protocol) ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="d3ded-151">Pour plus d’informations, consultez [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) et [à propos du protocole EAP (Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol)).</span><span class="sxs-lookup"><span data-stu-id="d3ded-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-152">Comment PEAP gère-t-il la reprise de session et la ré-authentification ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="d3ded-153">La réinitialisation et la réauthentification de la session se produisent généralement lors de l’itinérance sur un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="d3ded-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="d3ded-154">L’API de protection des données (DPAPI) Windows fournit un moyen de protéger et de lier des données à un utilisateur et éventuellement à la session de connexion.</span><span class="sxs-lookup"><span data-stu-id="d3ded-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="d3ded-155">L’appelant donne à [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) une mémoire tampon non chiffrée et DPAPI chiffre la mémoire en place.</span><span class="sxs-lookup"><span data-stu-id="d3ded-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="d3ded-156">Plus tard, l’appelant peut passer la mémoire tampon chiffrée à [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) et DPAPI déchiffrera la mémoire, une nouvelle fois en place.</span><span class="sxs-lookup"><span data-stu-id="d3ded-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="d3ded-157">Pour plus d’informations, voir [extension d’application interne TLS (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) et [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3ded-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-158">Qu’est-ce que la sécurité de niveau EAP-Transport (EAP-TLS) ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="d3ded-159">EAP-TLS est un protocole client-serveur dans lequel des profils de certificat distincts sont généralement utilisés pour le client et le serveur. Pour plus d’informations, consultez [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="d3ded-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-160">Comment faire implémenter une modification de mot de passe à l’aide de l’API LSA (local Security Authority) ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="d3ded-161">Utilisez la fonction [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) pour implémenter une modification de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d3ded-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-162">Pourquoi voulez-vous activer le suivi dans EAPHost ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="d3ded-163">Les journaux de suivi contiennent des informations de débogage (disponibles en anglais uniquement) qui peuvent aider les développeurs et les partenaires Microsoft à trouver les causes racines des problèmes rencontrés avec le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d3ded-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="d3ded-164">Pour plus d’informations, consultez [activation du suivi](enabling-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="d3ded-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-165">Pourquoi est-ce que je rencontre le code d’erreur NTE_BAD_KEY_STATE (0x8009000BL) lorsque j’utilise l’API de [chiffrement](/windows/desktop/SecCrypto/cryptography-portal) pour se connecter à l’échange EAP-TLS ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="d3ded-166">Dans Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) est défini en tant que &quot; clé non valide pour une utilisation dans l’état spécifié &quot; .</span><span class="sxs-lookup"><span data-stu-id="d3ded-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="d3ded-167">Cette erreur est généralement retournée dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="d3ded-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="d3ded-168">Lors d’une tentative d’exportation d’un objet BLOB de clé privée non exportable</span><span class="sxs-lookup"><span data-stu-id="d3ded-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="d3ded-169">En cas de tentative infructueuse de génération d’un handle de hachage de fonction Pseudo-aléatoire (PRF) à l’aide de [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/WinCrypt/NF-WinCrypt-CryptCreateHash)</span><span class="sxs-lookup"><span data-stu-id="d3ded-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="d3ded-170">Pour plus d’informations, consultez [terminer les messages dans le protocole TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="d3ded-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ded-171">Qu’est-ce qu’une fonction Pseudo-aléatoire (PRF) ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="d3ded-172">Fonction qui prend une clé, une étiquette et une valeur initiale comme entrée, puis produit une sortie de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d3ded-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="d3ded-173">Pour plus d’informations, consultez [terminer les messages dans le protocole TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="d3ded-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ded-174">Comment EAPHost est-il lié aux cartes réseau ?</span><span class="sxs-lookup"><span data-stu-id="d3ded-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="d3ded-175">EAPHost permet à plusieurs demandeurs de fonctionner simultanément, et chaque demandeur peut se lier à plusieurs cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="d3ded-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="d3ded-176">Les demandeurs EAPHost fournissent une liaison avec les couches réseau et pilotent le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d3ded-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="d3ded-177">Les demandeurs contiennent une configuration d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d3ded-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="d3ded-178">Les demandeurs enregistrent également l’État et fournissent la sécurité de connexion suivante.</span><span class="sxs-lookup"><span data-stu-id="d3ded-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="d3ded-179">Comme EAPHost n’est pas directement lié à un mécanisme réseau, l’extensibilité du demandeur est possible.</span><span class="sxs-lookup"><span data-stu-id="d3ded-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d3ded-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3ded-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3ded-181">FAQ du demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="d3ded-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="d3ded-182">FAQ sur les méthodes EAPHost</span><span class="sxs-lookup"><span data-stu-id="d3ded-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="d3ded-183">FAQ sur le développement EAPHost</span><span class="sxs-lookup"><span data-stu-id="d3ded-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

