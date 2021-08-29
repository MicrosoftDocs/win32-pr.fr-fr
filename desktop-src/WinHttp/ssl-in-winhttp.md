---
description: les Services HTTP Microsoft Windows (WinHTTP) prennent en charge les transactions SSL (Secure Sockets Layer) (SSL), y compris les certificats clients. Cette rubrique décrit les concepts impliqués dans une transaction SSL et la façon dont ils sont gérés à l’aide de WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a041d55de85250edb1932aa3df4d114af8ef89fce6e56c3763cb235168b65be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133032"
---
# <a name="ssl-in-winhttp"></a>SSL dans WinHTTP

les Services HTTP Microsoft Windows (WinHTTP) prennent en charge les transactions SSL (Secure Sockets Layer) (SSL), y compris les certificats clients. Cette rubrique décrit les concepts impliqués dans une transaction SSL et la façon dont ils sont gérés à l’aide de WinHTTP.

## <a name="secure-sockets-layer"></a>protocole SSL

SSL est une norme établie pour garantir des transactions HTTP sécurisées. Le protocole SSL fournit un mécanisme permettant d’effectuer jusqu’au chiffrement 128 bits sur toutes les transactions entre le client et le serveur. Il permet au client de vérifier que le serveur appartient à une entité approuvée à l’aide de certificats de serveur. Il permet également au serveur de confirmer l’identité du client avec des certificats clients.

Chacun de ces problèmes de chiffrement, d’identité du serveur et d’identité du client est négocié dans le protocole de transfert SSL qui se produit lorsqu’un client demande d’abord une ressource à partir d’un serveur HTTPs (Secure Hypertext Transfer Protocol). Fondamentalement, le client et le serveur présentent chacun une liste de paramètres requis et préférés. Si un ensemble commun d’exigences peut être approuvé et respecté, une connexion SSL est établie.

WinHTTP fournit une interface de haut niveau pour l’utilisation de SSL. Bien que les détails de la négociation et de la transaction SSL soient gérés en interne, WinHTTP vous permet de récupérer les niveaux de chiffrement, de spécifier le protocole de sécurité et d’interagir avec les certificats serveur et client. Les sections suivantes fournissent des détails sur la création d’applications basées sur WinHTTP qui choisissent une version de protocole SSL, examinent les certificats de serveur et sélectionnent les certificats clients à envoyer aux serveurs HTTPs.

## <a name="server-certificates"></a>Certificats de serveur

Les certificats de serveur sont envoyés du serveur au client afin que le client puisse obtenir une clé publique pour le serveur et s’assurer que le serveur a été vérifié par une autorité de certification. Les certificats peuvent contenir des types différents de données. Par exemple, un certificat X. 509 comprend le format du certificat, le numéro de série du certificat, l’algorithme utilisé pour signer le certificat, le nom de l’autorité de certification qui a émis le certificat, le nom et la clé publique de l’entité qui demande le certificat et la signature de l’autorité de certification.

Lorsque vous utilisez l’interface de programmation d’applications (API) WinHTTP, vous pouvez récupérer un certificat de serveur en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et en spécifiant l’option WinHTTP de l’indicateur de [**struct de \_ \_ \_ certificat \_ de sécurité**](option-flags.md) . Le certificat de serveur est retourné dans une structure d' [**\_ \_ informations de certificat WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Si vous préférez récupérer le contexte de certificat, spécifiez l’indicateur de contexte de certificat de serveur de l' [**\_ option \_ \_ \_ WinHTTP**](option-flags.md) à la place.

Si un certificat de serveur contient des erreurs, des détails sur l’erreur peuvent être obtenus dans la fonction de rappel d’État. La notification d' [**\_ \_ \_ \_ échec sécurisé de l’état du rappel WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) indique une erreur avec un certificat de serveur. Le paramètre *lpvStatusInformation* contient un ou plusieurs indicateurs d’erreur détaillés. Pour plus d’informations, consultez la page [**\_ \_ rappel d’État WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .

## <a name="client-certificates"></a>Certificats clients

Au cours de la négociation SSL, le serveur peut nécessiter une authentification. Le client est authentifié en fournissant un certificat client valide au serveur. WinHTTP vous permet de sélectionner et d’envoyer un certificat à partir d’un [*magasin de certificats*](glossary.md)local. Les sections suivantes décrivent le processus qui fournit des certificats clients lors de l’utilisation de l’API WinHTTP ou de l’objet [**WinHttpRequest**](winhttprequest.md) .

### <a name="winhttp-api"></a>API WinHTTP

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) et [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) peuvent tous les deux échouer pour indiquer qu’une demande a échoué, car le serveur HTTPS nécessite une authentification. Dans ce cas, Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour retourne le \_ \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire. Une fois cette erreur reçue, utilisez les fonctions [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) appropriées pour rechercher un certificat approprié. Indiquez que ce certificat doit être envoyé avec la requête suivante en appelant [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l' [**option WinHTTP indicateur de \_ \_ \_ \_ contexte CERT client**](option-flags.md) .

L’exemple de code suivant montre comment ouvrir un [*magasin de certificats*](glossary.md) et Rechercher un certificat basé sur le nom du sujet après l’erreur le certificat d' \_ authentification du \_ client WinHTTP \_ \_ \_ requis a été retourné.


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



Avant de renvoyer une demande contenant un certificat client, vous pouvez déterminer si le niveau de chiffrement pris en charge est acceptable pour votre application. Appelez [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et spécifiez [**l' \_ option \_ WinHTTP \_ indicateurs de sécurité indicateurs de sécurité**](option-flags.md) pour déterminer le niveau de chiffrement utilisé.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Récupération de la liste d’émetteurs pour l’authentification du client SSL

Lorsque l’application cliente WinHttp envoie une demande à un serveur HTTP sécurisé qui requiert l’authentification du client SSL, WinHttp retourne une erreur que le certificat d' **\_ authentification du client WinHTTP a \_ \_ \_ \_ requis** si l’application n’a pas fourni de certificat client. pour les ordinateurs qui exécutent sur Windows Server 2008 et Windows Vista, WinHttp permet à l’application de récupérer la liste d’émetteurs de certificats fournie par le serveur dans le test d’authentification. La liste d’émetteurs spécifie une liste d’autorités de certification autorisées par le serveur pour émettre des certificats clients. L’application filtre la liste d’émetteurs pour obtenir le certificat requis.

L’application cliente WinHttp récupère la liste d’émetteurs quand [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne **un \_ certificat d’authentification de \_ client WinHTTP \_ \_ \_ nécessaire**. Lorsque cette erreur est retournée, l’application appelle [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) à l’aide de l’option **WinHTTP liste d' \_ \_ \_ \_ émetteurs \_ de certificats client** . Le paramètre *lpBuffer* doit être suffisamment grand pour contenir un pointeur vers la structure [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) . L’exemple de code suivant montre comment récupérer la liste d’émetteurs.


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



Les informations de la structure [SecPkgContext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cIssuers* et *aIssuers*, peuvent être utilisées pour rechercher le certificat comme indiqué dans l’exemple de code ci-dessous. Pour plus d’informations, consultez [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


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



### <a name="optional-client-ssl-certificates"></a>Certificats SSL client facultatifs

à partir de Windows Server 2008 et Windows Vista, l’API WinHttp prend en charge les certificats clients facultatifs. Lorsque le serveur demande un certificat client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne une erreur message d' **authentification du \_ \_ client WinHTTP \_ \_ \_ requis** . Si le serveur demande le certificat, mais ne l’exige pas, l’application peut spécifier cette option pour indiquer qu’elle n’a pas de certificat. Le serveur peut choisir un autre schéma d’authentification ou autoriser un accès anonyme au serveur. L’application spécifie la macro de **\_ \_ \_ \_ contexte de certificat non client WinHTTP** dans le paramètre *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , comme indiqué dans l’exemple de code suivant.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Si le **\_ \_ \_ \_ contexte de certificat client WinHTTP n’est pas** défini et que le serveur requiert toujours un certificat client, il peut envoyer un code d’état HTTP 403. Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .

### <a name="winhttprequest-object"></a>Objet WinHttpRequest

Utilisez la méthode [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) de l’objet [**WinHttpRequest**](winhttprequest.md) pour sélectionner les certificats clients à envoyer au serveur à l’aide d’une demande. Sélectionnez un certificat en spécifiant une chaîne de sélection de certificat à l’aide de la méthode [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) . La chaîne de sélection de certificat se compose de l’emplacement du certificat, du [*magasin de certificats*](glossary.md)et du nom d’objet délimités par des barres obliques inverses. Le tableau suivant répertorie les composants de cette chaîne de sélection.



| Composant                                                  | Description                                                                                                                                                                                        | Valeurs possibles                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Emplacement                                                   | Détermine la clé de Registre sous laquelle les certificats sont stockés.                                                                                                                               | Les valeurs possibles sont « \_ ordinateur local » pour indiquer que le [*magasin de certificats*](glossary.md) se trouve sous **HKEY \_ local \_ machine**<br/> et « \_ utilisateur actuel » pour indiquer que le *magasin de certificats* se trouve sous l'**\_ utilisateur HKEY actuel \_** sans emprunt d’identité.<br/> Ce composant respecte la casse. |
| [*Magasin de certificats*](glossary.md) | Indique le nom du [*magasin de certificats*](glossary.md) qui contient le certificat approprié.                                                                       | Les [*magasins de certificats*](glossary.md) standard sont « My », « root » et « TrustedPeople ». Ce composant respecte la casse.                                                                                                                                                                                          |
| Nom d'objet                                               | Identifie un certificat dans le [*magasin de certificats*](glossary.md)spécifié. Le premier certificat qui contient la chaîne spécifiée pour ce composant est sélectionné. | Le nom du sujet peut être n’importe quelle chaîne. Une chaîne vide indique que le premier certificat du [*magasin de certificats*](glossary.md) doit être utilisé. Ce composant ne respecte pas la casse.                                                                                                                         |



 

Le nom et l’emplacement du [*magasin de certificats*](glossary.md) sont des composants facultatifs. Toutefois, si vous spécifiez un *magasin de certificats*, vous devez également spécifier l’emplacement de ce magasin de *certificats*. L’emplacement par défaut est \_ utilisateur actuel et le *magasin de certificats* par défaut est « My ».

L’exemple de code suivant montre comment spécifier qu’un certificat avec le sujet « My Middle-Tier Certificate » doit être choisi dans le magasin de [*certificats*](glossary.md) « personnel » dans le Registre sous **HKEY \_ local \_ machine**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> Dans certains langages, la barre oblique inverse est un caractère d’échappement. N’oubliez pas de modifier la chaîne de sélection du certificat afin de prendre en compte cette valeur. par exemple, dans Microsoft JScript, utilisez deux barres obliques inverses contiguës au lieu d’une.

 

Si vous ne spécifiez pas de certificat et qu’un serveur HTTPs requiert un certificat client, WinHTTP sélectionne le premier certificat dans le [*magasin de certificats*](glossary.md)par défaut. Si aucun certificat n’existe, une erreur est générée. Si le certificat n’est pas accepté, le serveur renvoie un code d’état 403 pour indiquer que la demande ne peut pas être satisfaite. Vous pouvez ensuite choisir un certificat plus approprié avec [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) et renvoyer la demande.

 

