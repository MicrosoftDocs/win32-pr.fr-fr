---
description: Une attention particulière doit être prise en compte lors de l’utilisation du fournisseur SSP (Security Support Provider) Kerberos si l’interopérabilité avec GSSAPI est requise.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interopérabilité SSPI/Kerberos avec GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749597"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="ee3f8-103">Interopérabilité SSPI/Kerberos avec GSSAPI</span><span class="sxs-lookup"><span data-stu-id="ee3f8-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="ee3f8-104">Une attention particulière doit être prise en compte lors de l’utilisation du fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) [*Kerberos*](../secgloss/k-gly.md) si l’interopérabilité avec GSSAPI est requise.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="ee3f8-105">Les conventions de code suivantes permettent l’interopérabilité avec des applications basées sur GSSAPI :</span><span class="sxs-lookup"><span data-stu-id="ee3f8-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="ee3f8-106">Noms compatibles Windows</span><span class="sxs-lookup"><span data-stu-id="ee3f8-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="ee3f8-107">Authentification</span><span class="sxs-lookup"><span data-stu-id="ee3f8-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="ee3f8-108">Intégrité et confidentialité des messages</span><span class="sxs-lookup"><span data-stu-id="ee3f8-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="ee3f8-109">Vous trouverez des exemples de code dans le kit de développement logiciel (SDK) de la plateforme sous exemples de \\ sécurité \\ SSPI \\ GSS.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="ee3f8-110">En outre, l’exemple UNIX équivalent est distribué dans les distributions Kerberos MIT et heimdal, client et serveur GSS.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="ee3f8-111">Noms de Windows-Compatible</span><span class="sxs-lookup"><span data-stu-id="ee3f8-111">Windows-Compatible Names</span></span>

<span data-ttu-id="ee3f8-112">Les fonctions GSSAPI utilisent un format de nom connu \_ sous \_ le nom de service GSS NT \_ , tel que spécifié dans la RFC.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="ee3f8-113">Par exemple, sample@host.dom.com est un nom qui peut être utilisé dans une application GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="ee3f8-114">Le système d’exploitation Windows ne reconnaît pas le \_ format de nom de service GSS NT \_ \_ , et le [*nom de principal du service*](../secgloss/s-gly.md)complet, par exemple sample/host.dom.com@REALM , doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="ee3f8-115">Authentification</span><span class="sxs-lookup"><span data-stu-id="ee3f8-115">Authentication</span></span>

<span data-ttu-id="ee3f8-116">L’authentification est généralement gérée lorsqu’une connexion est configurée pour la première fois entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="ee3f8-117">Dans cet exemple, le client utilise l' [*interface SSPI (Security Support Provider Interface*](../secgloss/s-gly.md) ) et le serveur utilise GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="ee3f8-118">**Pour configurer l’authentification dans le client SSPI**</span><span class="sxs-lookup"><span data-stu-id="ee3f8-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="ee3f8-119">Accédez aux [*informations d’identification*](../secgloss/c-gly.md) sortantes à l’aide de [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="ee3f8-120">Créez un nom de service avec **GSS \_ import \_ Name ()** et obtenez les informations d’identification entrantes à l’aide de **GSS \_ Acquire \_ cred**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="ee3f8-121">Obtient un jeton d’authentification à envoyer au serveur à l’aide de [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="ee3f8-122">Envoyez le jeton au serveur.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-122">Send the token to the server.</span></span>

<span data-ttu-id="ee3f8-123">**Pour configurer l’authentification dans le serveur GSSAPI**</span><span class="sxs-lookup"><span data-stu-id="ee3f8-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="ee3f8-124">Analyser le message du client pour extraire le jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="ee3f8-125">Utilisez la fonction de **\_ \_ \_ contexte GSS Accept sec** , en passant le jeton en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="ee3f8-126">Analysez le message à partir du serveur pour extraire le jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="ee3f8-127">Transmettez ce jeton de sécurité à [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="ee3f8-128">Envoyer un jeton de réponse au client.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-128">Send a response token to the client.</span></span>

    <span data-ttu-id="ee3f8-129">La fonction de **\_ \_ \_ contexte GSS Accept sec** peut retourner un jeton que vous pouvez renvoyer au client.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="ee3f8-130">S’il est nécessaire de continuer, envoyez un jeton de réponse au serveur. dans le cas contraire, la configuration de l’authentification est terminée.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="ee3f8-131">S’il est nécessaire de continuer, attendez le jeton suivant du client. dans le cas contraire, la configuration de l’authentification est terminée.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="ee3f8-132">Intégrité et confidentialité des messages</span><span class="sxs-lookup"><span data-stu-id="ee3f8-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="ee3f8-133">La plupart des applications basées sur GSSAPI utilisent la fonction **GSS \_ Wrap** pour signer un message avant de l’envoyer.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="ee3f8-134">À l’inverse, la fonction de **\_ désencapsulage GSS** vérifie la signature.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="ee3f8-135">**GSS \_ Wrap** est disponible dans la version 2,0 de l’API et est désormais largement utilisé et spécifié dans les normes Internet qui décrivent l’utilisation de GSSAPI pour l’ajout de la sécurité aux protocoles.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="ee3f8-136">Précédemment, les fonctions GSS **SignMessage** et **SealMessage** étaient utilisées pour [*l’intégrité*](../secgloss/i-gly.md) et la [*confidentialité*](../secgloss/p-gly.md)des messages.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="ee3f8-137">**GSS \_ Wrap** et **GSS \_ Unwrap** sont utilisés à des fins d’intégrité et de confidentialité avec l’utilisation de la confidentialité contrôlée par la valeur de l’argument « conf \_ Flag ».</span><span class="sxs-lookup"><span data-stu-id="ee3f8-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="ee3f8-138">Si un protocole GSSAPI est spécifié pour utiliser les fonctions **GSS \_ obtenir \_ MIC** et **GSS \_ verify \_** , les fonctions SSPI appropriées sont [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="ee3f8-139">Sachez que **MakeSignature** et **VerifySignature** n’interagissent pas avec **GSS \_ Wrap** lorsque l' \_ indicateur conf est défini sur zéro ou avec **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="ee3f8-140">Il en va de même pour mélanger [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour la signature uniquement et le **\_ \_ MIC Verify**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="ee3f8-141">N’utilisez pas les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) ou [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) lorsque les fonctions **GSS \_ Wrap** et **GSS \_ Unwrap** sont appelées pour.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="ee3f8-142">L’équivalent SSPI de **GSS \_ Wrap** est [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour l’intégrité et la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="ee3f8-143">L’exemple suivant illustre l’utilisation de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour signer les données qui seront vérifiées par le déchiffrement **GSS \_**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="ee3f8-144">Dans le client SSPI :</span><span class="sxs-lookup"><span data-stu-id="ee3f8-144">In the SSPI client:</span></span>


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



<span data-ttu-id="ee3f8-145">Dans le serveur GSSAPI :</span><span class="sxs-lookup"><span data-stu-id="ee3f8-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="ee3f8-146">L’équivalent SSPI de **GSS \_ Unwrap** est [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="ee3f8-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="ee3f8-147">Voici un exemple qui montre comment utiliser **DecryptMessage (Kerberos)** pour déchiffrer les données qui ont été chiffrées par le protocole **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="ee3f8-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="ee3f8-148">Dans le serveur GSSAPI :</span><span class="sxs-lookup"><span data-stu-id="ee3f8-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="ee3f8-149">Dans le client SSPI :</span><span class="sxs-lookup"><span data-stu-id="ee3f8-149">In the SSPI client:</span></span>


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 
