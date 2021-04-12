---
description: Les services HTTP Microsoft Windows (WinHTTP) prennent en charge les transactions SSL (Secure Sockets Layer) (SSL), y compris les certificats clients. Cette rubrique décrit les concepts impliqués dans une transaction SSL et la façon dont ils sont gérés à l’aide de WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203359"
---
# <a name="ssl-in-winhttp"></a><span data-ttu-id="dc92e-104">SSL dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dc92e-104">SSL in WinHTTP</span></span>

<span data-ttu-id="dc92e-105">Les services HTTP Microsoft Windows (WinHTTP) prennent en charge les transactions SSL (Secure Sockets Layer) (SSL), y compris les certificats clients.</span><span class="sxs-lookup"><span data-stu-id="dc92e-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="dc92e-106">Cette rubrique décrit les concepts impliqués dans une transaction SSL et la façon dont ils sont gérés à l’aide de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="dc92e-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="dc92e-107">protocole SSL</span><span class="sxs-lookup"><span data-stu-id="dc92e-107">Secure Sockets Layer</span></span>

<span data-ttu-id="dc92e-108">SSL est une norme établie pour garantir des transactions HTTP sécurisées.</span><span class="sxs-lookup"><span data-stu-id="dc92e-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="dc92e-109">Le protocole SSL fournit un mécanisme permettant d’effectuer jusqu’au chiffrement 128 bits sur toutes les transactions entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="dc92e-110">Il permet au client de vérifier que le serveur appartient à une entité approuvée à l’aide de certificats de serveur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="dc92e-111">Il permet également au serveur de confirmer l’identité du client avec des certificats clients.</span><span class="sxs-lookup"><span data-stu-id="dc92e-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="dc92e-112">Chacun de ces problèmes de chiffrement, d’identité du serveur et d’identité du client est négocié dans le protocole de transfert SSL qui se produit lorsqu’un client demande d’abord une ressource à partir d’un serveur HTTPs (Secure Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="dc92e-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="dc92e-113">Fondamentalement, le client et le serveur présentent chacun une liste de paramètres requis et préférés.</span><span class="sxs-lookup"><span data-stu-id="dc92e-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="dc92e-114">Si un ensemble commun d’exigences peut être approuvé et respecté, une connexion SSL est établie.</span><span class="sxs-lookup"><span data-stu-id="dc92e-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="dc92e-115">WinHTTP fournit une interface de haut niveau pour l’utilisation de SSL.</span><span class="sxs-lookup"><span data-stu-id="dc92e-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="dc92e-116">Bien que les détails de la négociation et de la transaction SSL soient gérés en interne, WinHTTP vous permet de récupérer les niveaux de chiffrement, de spécifier le protocole de sécurité et d’interagir avec les certificats serveur et client.</span><span class="sxs-lookup"><span data-stu-id="dc92e-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="dc92e-117">Les sections suivantes fournissent des détails sur la création d’applications basées sur WinHTTP qui choisissent une version de protocole SSL, examinent les certificats de serveur et sélectionnent les certificats clients à envoyer aux serveurs HTTPs.</span><span class="sxs-lookup"><span data-stu-id="dc92e-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="dc92e-118">Certificats de serveur</span><span class="sxs-lookup"><span data-stu-id="dc92e-118">Server Certificates</span></span>

<span data-ttu-id="dc92e-119">Les certificats de serveur sont envoyés du serveur au client afin que le client puisse obtenir une clé publique pour le serveur et s’assurer que le serveur a été vérifié par une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dc92e-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="dc92e-120">Les certificats peuvent contenir des types différents de données.</span><span class="sxs-lookup"><span data-stu-id="dc92e-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="dc92e-121">Par exemple, un certificat X. 509 comprend le format du certificat, le numéro de série du certificat, l’algorithme utilisé pour signer le certificat, le nom de l’autorité de certification qui a émis le certificat, le nom et la clé publique de l’entité qui demande le certificat et la signature de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dc92e-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="dc92e-122">Lorsque vous utilisez l’interface de programmation d’applications (API) WinHTTP, vous pouvez récupérer un certificat de serveur en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et en spécifiant l’option WinHTTP de l’indicateur de [**struct de \_ \_ \_ certificat \_ de sécurité**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="dc92e-123">Le certificat de serveur est retourné dans une structure d' [**\_ \_ informations de certificat WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="dc92e-124">Si vous préférez récupérer le contexte de certificat, spécifiez l’indicateur de contexte de certificat de serveur de l' [**\_ option \_ \_ \_ WinHTTP**](option-flags.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="dc92e-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="dc92e-125">Si un certificat de serveur contient des erreurs, des détails sur l’erreur peuvent être obtenus dans la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="dc92e-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="dc92e-126">La notification d' [**\_ \_ \_ \_ échec sécurisé de l’état du rappel WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indique une erreur avec un certificat de serveur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="dc92e-127">Le paramètre *lpvStatusInformation* contient un ou plusieurs indicateurs d’erreur détaillés.</span><span class="sxs-lookup"><span data-stu-id="dc92e-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="dc92e-128">Pour plus d’informations, consultez la page [**\_ \_ rappel d’État WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="dc92e-129">Certificats clients</span><span class="sxs-lookup"><span data-stu-id="dc92e-129">Client Certificates</span></span>

<span data-ttu-id="dc92e-130">Au cours de la négociation SSL, le serveur peut nécessiter une authentification.</span><span class="sxs-lookup"><span data-stu-id="dc92e-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="dc92e-131">Le client est authentifié en fournissant un certificat client valide au serveur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="dc92e-132">WinHTTP vous permet de sélectionner et d’envoyer un certificat à partir d’un [*magasin de certificats*](glossary.md)local.</span><span class="sxs-lookup"><span data-stu-id="dc92e-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="dc92e-133">Les sections suivantes décrivent le processus qui fournit des certificats clients lors de l’utilisation de l’API WinHTTP ou de l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="dc92e-134">API WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dc92e-134">WinHTTP API</span></span>

<span data-ttu-id="dc92e-135">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) et [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) peuvent tous les deux échouer pour indiquer qu’une demande a échoué, car le serveur HTTPS nécessite une authentification.</span><span class="sxs-lookup"><span data-stu-id="dc92e-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="dc92e-136">Dans ce cas, Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour retourne le \_ \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dc92e-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="dc92e-137">Une fois cette erreur reçue, utilisez les fonctions [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) appropriées pour rechercher un certificat approprié.</span><span class="sxs-lookup"><span data-stu-id="dc92e-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="dc92e-138">Indiquez que ce certificat doit être envoyé avec la requête suivante en appelant [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l' [**option WinHTTP indicateur de \_ \_ \_ \_ contexte CERT client**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="dc92e-139">L’exemple de code suivant montre comment ouvrir un [*magasin de certificats*](glossary.md) et Rechercher un certificat basé sur le nom du sujet après l’erreur le certificat d' \_ authentification du \_ client WinHTTP \_ \_ \_ requis a été retourné.</span><span class="sxs-lookup"><span data-stu-id="dc92e-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



<span data-ttu-id="dc92e-140">Avant de renvoyer une demande contenant un certificat client, vous pouvez déterminer si le niveau de chiffrement pris en charge est acceptable pour votre application.</span><span class="sxs-lookup"><span data-stu-id="dc92e-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="dc92e-141">Appelez [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et spécifiez [**l' \_ option \_ WinHTTP \_ indicateurs de sécurité indicateurs de sécurité**](option-flags.md) pour déterminer le niveau de chiffrement utilisé.</span><span class="sxs-lookup"><span data-stu-id="dc92e-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="dc92e-142">Récupération de la liste d’émetteurs pour l’authentification du client SSL</span><span class="sxs-lookup"><span data-stu-id="dc92e-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="dc92e-143">Lorsque l’application cliente WinHttp envoie une demande à un serveur HTTP sécurisé qui requiert l’authentification du client SSL, WinHttp retourne une erreur que le certificat d' **\_ authentification du client WinHTTP a \_ \_ \_ \_ requis** si l’application n’a pas fourni de certificat client.</span><span class="sxs-lookup"><span data-stu-id="dc92e-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="dc92e-144">Pour les ordinateurs qui exécutent Windows Server 2008 et Windows Vista, WinHttp permet à l’application de récupérer la liste d’émetteurs de certificats fournie par le serveur dans la demande d’authentification.</span><span class="sxs-lookup"><span data-stu-id="dc92e-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="dc92e-145">La liste d’émetteurs spécifie une liste d’autorités de certification autorisées par le serveur pour émettre des certificats clients.</span><span class="sxs-lookup"><span data-stu-id="dc92e-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="dc92e-146">L’application filtre la liste d’émetteurs pour obtenir le certificat requis.</span><span class="sxs-lookup"><span data-stu-id="dc92e-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="dc92e-147">L’application cliente WinHttp récupère la liste d’émetteurs quand [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne **un \_ certificat d’authentification de \_ client WinHTTP \_ \_ \_ nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="dc92e-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="dc92e-148">Lorsque cette erreur est retournée, l’application appelle [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) à l’aide de l’option **WinHTTP liste d' \_ \_ \_ \_ émetteurs \_ de certificats client** .</span><span class="sxs-lookup"><span data-stu-id="dc92e-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="dc92e-149">Le paramètre *lpBuffer* doit être suffisamment grand pour contenir un pointeur vers la structure [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="dc92e-150">L’exemple de code suivant montre comment récupérer la liste d’émetteurs.</span><span class="sxs-lookup"><span data-stu-id="dc92e-150">The following code example shows how to retrieve the issuer list.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



<span data-ttu-id="dc92e-151">Les informations de la structure [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* et *aIssuers*, peuvent être utilisées pour rechercher le certificat comme indiqué dans l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dc92e-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="dc92e-152">Pour plus d’informations, consultez [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="dc92e-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="dc92e-153">Certificats SSL client facultatifs</span><span class="sxs-lookup"><span data-stu-id="dc92e-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="dc92e-154">À compter de Windows Server 2008 et Windows Vista, l’API WinHttp prend en charge les certificats clients facultatifs.</span><span class="sxs-lookup"><span data-stu-id="dc92e-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="dc92e-155">Lorsque le serveur demande un certificat client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne une erreur message d' **authentification du \_ \_ client WinHTTP \_ \_ \_ requis** .</span><span class="sxs-lookup"><span data-stu-id="dc92e-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="dc92e-156">Si le serveur demande le certificat, mais ne l’exige pas, l’application peut spécifier cette option pour indiquer qu’elle n’a pas de certificat.</span><span class="sxs-lookup"><span data-stu-id="dc92e-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="dc92e-157">Le serveur peut choisir un autre schéma d’authentification ou autoriser un accès anonyme au serveur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="dc92e-158">L’application spécifie la macro de **\_ \_ \_ \_ contexte de certificat non client WinHTTP** dans le paramètre *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="dc92e-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="dc92e-159">Si le **\_ \_ \_ \_ contexte de certificat client WinHTTP n’est pas** défini et que le serveur requiert toujours un certificat client, il peut envoyer un code d’état HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="dc92e-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="dc92e-160">Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .</span><span class="sxs-lookup"><span data-stu-id="dc92e-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="dc92e-161">Objet WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="dc92e-161">WinHttpRequest Object</span></span>

<span data-ttu-id="dc92e-162">Utilisez la méthode [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) de l’objet [**WinHttpRequest**](winhttprequest.md) pour sélectionner les certificats clients à envoyer au serveur à l’aide d’une demande.</span><span class="sxs-lookup"><span data-stu-id="dc92e-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="dc92e-163">Sélectionnez un certificat en spécifiant une chaîne de sélection de certificat à l’aide de la méthode [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="dc92e-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="dc92e-164">La chaîne de sélection de certificat se compose de l’emplacement du certificat, du [*magasin de certificats*](glossary.md)et du nom d’objet délimités par des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="dc92e-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="dc92e-165">Le tableau suivant répertorie les composants de cette chaîne de sélection.</span><span class="sxs-lookup"><span data-stu-id="dc92e-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="dc92e-166">Composant</span><span class="sxs-lookup"><span data-stu-id="dc92e-166">Component</span></span>                                                  | <span data-ttu-id="dc92e-167">Description</span><span class="sxs-lookup"><span data-stu-id="dc92e-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="dc92e-168">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="dc92e-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc92e-169">Emplacement</span><span class="sxs-lookup"><span data-stu-id="dc92e-169">Location</span></span>                                                   | <span data-ttu-id="dc92e-170">Détermine la clé de Registre sous laquelle les certificats sont stockés.</span><span class="sxs-lookup"><span data-stu-id="dc92e-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="dc92e-171">Les valeurs possibles sont « \_ ordinateur local » pour indiquer que le [*magasin de certificats*](glossary.md) se trouve sous **HKEY \_ local \_ machine**</span><span class="sxs-lookup"><span data-stu-id="dc92e-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="dc92e-172">et « \_ utilisateur actuel » pour indiquer que le *magasin de certificats* se trouve sous l'**\_ utilisateur HKEY actuel \_** sans emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="dc92e-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="dc92e-173">Ce composant respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="dc92e-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="dc92e-174">*Magasin de certificats*</span><span class="sxs-lookup"><span data-stu-id="dc92e-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="dc92e-175">Indique le nom du [*magasin de certificats*](glossary.md) qui contient le certificat approprié.</span><span class="sxs-lookup"><span data-stu-id="dc92e-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="dc92e-176">Les [*magasins de certificats*](glossary.md) standard sont « My », « root » et « TrustedPeople ».</span><span class="sxs-lookup"><span data-stu-id="dc92e-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="dc92e-177">Ce composant respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="dc92e-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="dc92e-178">Nom d'objet</span><span class="sxs-lookup"><span data-stu-id="dc92e-178">Subject name</span></span>                                               | <span data-ttu-id="dc92e-179">Identifie un certificat dans le [*magasin de certificats*](glossary.md)spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc92e-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="dc92e-180">Le premier certificat qui contient la chaîne spécifiée pour ce composant est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dc92e-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="dc92e-181">Le nom du sujet peut être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="dc92e-181">The subject name can be any string.</span></span> <span data-ttu-id="dc92e-182">Une chaîne vide indique que le premier certificat du [*magasin de certificats*](glossary.md) doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="dc92e-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="dc92e-183">Ce composant ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="dc92e-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="dc92e-184">Le nom et l’emplacement du [*magasin de certificats*](glossary.md) sont des composants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="dc92e-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="dc92e-185">Toutefois, si vous spécifiez un *magasin de certificats*, vous devez également spécifier l’emplacement de ce magasin de *certificats*.</span><span class="sxs-lookup"><span data-stu-id="dc92e-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="dc92e-186">L’emplacement par défaut est \_ utilisateur actuel et le *magasin de certificats* par défaut est « My ».</span><span class="sxs-lookup"><span data-stu-id="dc92e-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="dc92e-187">L’exemple de code suivant montre comment spécifier qu’un certificat avec le sujet « My Middle-Tier Certificate » doit être choisi dans le magasin de [*certificats*](glossary.md) « personnel » dans le Registre sous **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="dc92e-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="dc92e-188">Dans certains langages, la barre oblique inverse est un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="dc92e-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="dc92e-189">N’oubliez pas de modifier la chaîne de sélection du certificat afin de prendre en compte cette valeur.</span><span class="sxs-lookup"><span data-stu-id="dc92e-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="dc92e-190">Par exemple, dans Microsoft JScript, utilisez deux barres obliques inverses contiguës au lieu d’une.</span><span class="sxs-lookup"><span data-stu-id="dc92e-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="dc92e-191">Si vous ne spécifiez pas de certificat et qu’un serveur HTTPs requiert un certificat client, WinHTTP sélectionne le premier certificat dans le [*magasin de certificats*](glossary.md)par défaut.</span><span class="sxs-lookup"><span data-stu-id="dc92e-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="dc92e-192">Si aucun certificat n’existe, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="dc92e-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="dc92e-193">Si le certificat n’est pas accepté, le serveur renvoie un code d’état 403 pour indiquer que la demande ne peut pas être satisfaite.</span><span class="sxs-lookup"><span data-stu-id="dc92e-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="dc92e-194">Vous pouvez ensuite choisir un certificat plus approprié avec [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) et renvoyer la demande.</span><span class="sxs-lookup"><span data-stu-id="dc92e-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

