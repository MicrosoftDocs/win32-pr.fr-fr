---
title: Comment un client authentifie un service Windows Sockets SCP
description: Cette rubrique montre le code qu’une application cliente utilise pour composer un SPN pour un service.
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38471f48d8c80d0795b7176b95df0029d42325ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462019"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a><span data-ttu-id="548c5-103">Comment un client authentifie un service Windows Sockets SCP</span><span class="sxs-lookup"><span data-stu-id="548c5-103">How a Client Authenticates an SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="548c5-104">Cette rubrique montre le code qu’une application cliente utilise pour composer un SPN pour un service.</span><span class="sxs-lookup"><span data-stu-id="548c5-104">This topic shows the code that a client application uses to compose an SPN for a service.</span></span> <span data-ttu-id="548c5-105">Le client est lié au point de connexion de service (SCP) du service pour récupérer les données requises pour se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="548c5-105">The client binds to the service's service connection point (SCP) to retrieve the data required to connect to the service.</span></span> <span data-ttu-id="548c5-106">Le SCP contient également des données que le client peut utiliser pour composer le SPN du service.</span><span class="sxs-lookup"><span data-stu-id="548c5-106">The SCP also contains data that the client can use to compose the service's SPN.</span></span> <span data-ttu-id="548c5-107">Pour plus d’informations et pour obtenir un exemple de code qui crée une liaison avec le SCP et récupère les propriétés nécessaires, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="548c5-107">For more information and a code example that binds to the SCP and retrieves the necessary properties, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="548c5-108">Cette rubrique montre également comment un client utilise un package de sécurité SSPI et le SPN du service pour établir une connexion mutuellement authentifiée au service Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="548c5-108">This topic also shows how a client uses an SSPI security package and the service's SPN to establish a mutually authenticated connection to the Windows Sockets service.</span></span> <span data-ttu-id="548c5-109">N’oubliez pas que ce code est presque identique au code requis dans Microsoft Windows NT 4,0 et versions antérieures uniquement pour authentifier le client auprès du serveur.</span><span class="sxs-lookup"><span data-stu-id="548c5-109">Be aware that this code is almost identical to the code required in Microsoft Windows NT 4.0 and earlier just to authenticate the client to the server.</span></span> <span data-ttu-id="548c5-110">La seule différence est que le client doit fournir le nom de principal du service et spécifier l' \_ indicateur d’authentification mutuelle d’ISC req \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="548c5-110">The only difference is that the client must supply the SPN and specify the ISC\_REQ\_MUTUAL\_AUTH flag.</span></span>

## <a name="client-code-to-make-an-spn-for-a-service"></a><span data-ttu-id="548c5-111">Code client pour créer un SPN pour un service</span><span class="sxs-lookup"><span data-stu-id="548c5-111">Client Code to Make an SPN for a Service</span></span>


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a><span data-ttu-id="548c5-112">Code client pour authentifier le service</span><span class="sxs-lookup"><span data-stu-id="548c5-112">Client Code to Authenticate the Service</span></span>

<span data-ttu-id="548c5-113">Cet exemple de code se compose de deux routines : la sous- **authentification** et **GenClientContext**.</span><span class="sxs-lookup"><span data-stu-id="548c5-113">This code example consists of two routines: **DoAuthentication** and **GenClientContext**.</span></span> <span data-ttu-id="548c5-114">Après l’appel de [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) pour composer un SPN pour le service, le client passe le nom de principal du service (SPN) à la routine de sous- **authentification** , qui appelle le **GenClientContext** pour générer la mémoire tampon initiale à envoyer au service.</span><span class="sxs-lookup"><span data-stu-id="548c5-114">After calling [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) to compose an SPN for the service, the client passes the SPN to the **DoAuthentication** routine, which calls the **GenClientContext** to generate the initial buffer to send to the service.</span></span> <span data-ttu-id="548c5-115">La sous- **authentification** utilise le handle de socket pour envoyer la mémoire tampon et recevoir la réponse du service transmise au package SSPI par un autre appel à **GenClientContext**.</span><span class="sxs-lookup"><span data-stu-id="548c5-115">**DoAuthentication** uses the socket handle to send the buffer and receive the service's response passed to the SSPI package by another call to **GenClientContext**.</span></span> <span data-ttu-id="548c5-116">Cette boucle est répétée jusqu’à ce que l’authentification échoue ou **GenClientContext** définit un indicateur qui indique que l’authentification a réussi.</span><span class="sxs-lookup"><span data-stu-id="548c5-116">This loop is repeated until the authentication fails or **GenClientContext** sets a flag that indicates the authentication succeeded.</span></span>

<span data-ttu-id="548c5-117">La routine **GenClientContext** interagit avec le package SSPI pour générer les données d’authentification à envoyer au service et traiter les données reçues du service.</span><span class="sxs-lookup"><span data-stu-id="548c5-117">The **GenClientContext** routine interacts with the SSPI package to generate the authentication data to send to the service and process the data received from the service.</span></span> <span data-ttu-id="548c5-118">Les principaux composants des données d’authentification fournies par le client sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="548c5-118">The key components of the authentication data provided by the client include:</span></span>

-   <span data-ttu-id="548c5-119">Nom du principal du service qui identifie les informations d’identification que le service doit authentifier.</span><span class="sxs-lookup"><span data-stu-id="548c5-119">The service principal name which identifies the credentials that the service must authenticate.</span></span>
-   <span data-ttu-id="548c5-120">Informations d’identification du client.</span><span class="sxs-lookup"><span data-stu-id="548c5-120">The client's credentials.</span></span> <span data-ttu-id="548c5-121">La fonction [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) du package de sécurité extrait ces informations d’identification du contexte de sécurité du client établi à l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="548c5-121">The [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) function of the security package extracts these credentials from the client's security context established at logon.</span></span>
-   <span data-ttu-id="548c5-122">Pour demander une authentification mutuelle, le client doit spécifier l' \_ \_ indicateur d’authentification mutuelle req req \_ quand il appelle la fonction [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) pendant la routine **GenClientContext** .</span><span class="sxs-lookup"><span data-stu-id="548c5-122">To request mutual authentication, the client must specify the ISC\_REQ\_MUTUAL\_AUTH flag when it calls the [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) function during the **GenClientContext** routine.</span></span>


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
     (SEC_I_COMPLETE_AND_CONTINUE == ssStatus))  
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
            (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 




