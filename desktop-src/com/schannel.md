---
title: Schannel
description: Le package de sécurité Secure Channel (SChannel), dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ GSS \_ Schannel, prend en charge les protocoles basés sur une clé publique SSL (SSL (Secure Sockets Layer)) versions 2,0 et 3,0, le protocole TLS (Transport Layer Security) 1,0 et la technologie de communication privée (PCT) 1,0. TLS 1,0 est une version normalisée, légèrement modifiée, de SSL 3,0, qui a été publiée par l’IETF (Internet Engineering Task Force) en janvier 1999, dans le document RFC 2246. Dans la mesure où TLS a été standardisé, les développeurs sont encouragés à utiliser TLS plutôt que SSL. PCT est inclus uniquement à des fins de compatibilité descendante et ne doit pas être utilisé pour un nouveau développement. Lorsque le package de sécurité Schannel est utilisé, DCOM négocie automatiquement le meilleur protocole, en fonction des capacités du client et du serveur.
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ab40ed9d87013f646137e23ccc755dfdf9ab6b8f2ded367940b4ae630d7b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047847"
---
# <a name="schannel"></a>Schannel

Le package de sécurité Secure Channel (SChannel), dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ GSS \_ Schannel, prend en charge les protocoles basés sur une clé publique suivants : SSL (SSL (Secure Sockets Layer)) versions 2,0 et 3,0, TLS (Transport Layer Security) 1,0 et PCT (Private Communication Technology) 1,0. TLS 1,0 est une version normalisée, légèrement modifiée, de SSL 3,0, qui a été publiée par l’IETF (Internet Engineering Task Force) en janvier 1999, dans le document [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt). Dans la mesure où TLS a été standardisé, les développeurs sont encouragés à utiliser TLS plutôt que SSL. PCT est inclus uniquement à des fins de compatibilité descendante et ne doit pas être utilisé pour un nouveau développement. Lorsque le package de sécurité Schannel est utilisé, DCOM négocie automatiquement le meilleur protocole, en fonction des capacités du client et du serveur.

Les rubriques suivantes décrivent brièvement le protocole TLS et son fonctionnement avec DCOM.

-   [Quand utiliser TLS](#when-to-use-tls)
-   [Bref aperçu du fonctionnement du protocole TLS](#brief-overview-of-how-tls-works)
-   [Certificats X. 509](#x509-certificates)
    -   [Certificats clients](#client-certificates)
-   [Utilisation de TLS dans COM](#using-tls-in-com)
    -   [Comment un serveur définit la couverture de sécurité](#how-a-server-sets-the-security-blanket)
    -   [Comment un client définit la couverture de sécurité](#how-a-client-sets-the-security-blanket)
    -   [Modification de la couverture de sécurité par un client](#how-a-client-changes-the-security-blanket)
    -   [Exemple : le client modifie la couverture de sécurité](#example-client-changes-the-security-blanket)
-   [Rubriques connexes](#related-topics)

> [!Note]  
> Toutes les informations sur le protocole TLS dans ces sections s’appliquent également aux protocoles SSL et PCT.

 

## <a name="when-to-use-tls"></a>Quand utiliser TLS

TLS est la seule option de sécurité disponible lorsque les serveurs doivent prouver leur identité aux clients anonymes. Ceci est particulièrement important pour les sites Web qui souhaitent participer au commerce électronique, car il permet de protéger la transmission d’informations sensibles, telles que des numéros de carte de crédit. Le protocole TLS garantit que les clients de commerce électronique peuvent être certains de ceux avec qui ils travaillent, car ils reçoivent une preuve de l’identité du serveur. Il permet également au serveur de commerce électronique d’éviter d’avoir à se préoccuper de l’authentification de l’identité de chacun de ses clients.

TLS exige que tous les serveurs prouvent leur identité aux clients. En outre, TLS permet aux clients de prouver leur identité aux serveurs. Cette authentification mutuelle peut être utile pour limiter l’accès de certaines pages Web dans un intranet d’entreprise de grande taille.

Le protocole TLS prend en charge les niveaux d’authentification les plus élevés et offre une architecture ouverte qui permet d’augmenter la puissance de chiffrement au fil du temps pour suivre l’innovation technologique. TLS est le meilleur choix pour les environnements où le niveau de sécurité le plus élevé est souhaité pour les données en transit.

## <a name="brief-overview-of-how-tls-works"></a>Bref aperçu du fonctionnement du protocole TLS

Le protocole TLS repose sur une infrastructure à clé publique (PKI), qui utilise des paires de clés publiques/privées pour activer le chiffrement des données et établir l’intégrité des données, et utilise des certificats X. 509 pour l’authentification.

De nombreux protocoles de sécurité, tels que le protocole Kerberos V5, dépendent d’une clé unique pour chiffrer et déchiffrer les données. Ces protocoles dépendent donc de l’échange sécurisé des clés de chiffrement. dans le protocole Kerberos, cette opération s’effectue par le biais de tickets obtenus à partir du centre de distribution de clés (KDC). Cela exige que tout le monde qui utilise le protocole Kerberos soit inscrit auprès du KDC, ce qui constituerait une limitation impraticable pour un serveur Web de commerce électronique destiné à attirer des millions de clients dans le monde entier. Par conséquent, le protocole TLS repose sur une infrastructure à clé publique, qui utilise deux clés pour le encryptionâ de données» lorsqu’une clé de la paire chiffre les données, seule l’autre clé de la paire peut la déchiffrer. Le principal avantage de cette conception est que le chiffrement peut être effectué sans nécessiter l’échange sécurisé de clés de chiffrement.

Une infrastructure à clé publique utilise une technique dans laquelle l’une des clés est gardée privée et n’est disponible que pour le principal auquel elle est inscrite, tandis que l’autre clé est rendue publique pour quiconque peut y accéder. Si quelqu’un souhaite envoyer un message privé au propriétaire d’une paire de clés, le message peut être chiffré avec la clé publique et seule la clé privée peut être utilisée pour déchiffrer le message.

Les paires de clés sont également utilisées pour vérifier l’intégrité des données envoyées. Pour ce faire, le propriétaire de la paire de clés peut attacher une signature numérique aux données avant de les envoyer. La création d’une signature numérique implique le calcul d’un hachage des données et le chiffrement du hachage avec la clé privée. Toute personne qui utilise la clé publique pour déchiffrer la signature numérique est assurée que la signature numérique ne doit être fournie qu’à partir de la personne propriétaire de la clé privée. En outre, le destinataire peut calculer un hachage des données à l’aide du même algorithme que l’expéditeur, et si le hachage calculé correspond à celui envoyé dans la signature numérique, le destinataire peut être certain que les données n’ont pas été modifiées une fois qu’elles ont été signées numériquement.

L’un des inconvénients de l’utilisation d’une infrastructure à clé publique pour le chiffrement de données volumineux est que ses performances sont relativement lentes. En raison de l’activité mathématique intensive impliquée, le chiffrement et le déchiffrement des données à l’aide d’un chiffrement asymétrique qui dépend d’une paire de clés peuvent être jusqu’à 1 000 fois plus lents que le chiffrement et le déchiffrement à l’aide d’un chiffrement symétrique qui dépend uniquement d’une clé unique. Par conséquent, TLS utilise une infrastructure à clé publique uniquement pour générer des signatures numériques et pour négocier la clé unique spécifique à la session qui sera utilisée par le client et le serveur pour le chiffrement et le déchiffrement des données en bloc. Le protocole TLS prend en charge une grande variété de chiffrements symétriques à une seule clé, et des chiffrements supplémentaires peuvent être ajoutés à l’avenir.

Pour plus d’informations sur le protocole de négociation TLS, consultez [protocole de négociation TLS](/windows/desktop/SecAuthN/tls-handshake-protocol).

Pour plus d’informations sur le chiffrement derrière le protocole TLS, consultez la page sur la [cryptographie Essentials](/windows/desktop/SecCrypto/cryptography-essentials).

## <a name="x509-certificates"></a>Certificats X.509

Un problème critique qui doit être traité par une infrastructure à clé publique est la possibilité d’approuver l’authenticité de la clé publique utilisée. Lorsque vous utilisez une clé publique émise pour une société avec laquelle vous souhaitez faire des affaires, vous devez être certain que la clé appartient réellement à la société plutôt qu’à un voleur qui souhaite découvrir le numéro de votre carte de crédit.

Pour garantir l’identité d’un principal contenant une paire de clés, un certificat X. 509 est émis par une autorité de certification (CA). Ce certificat contient des informations qui identifient le principal, contient la clé publique du principal et est signée numériquement par l’autorité de certification. Cette signature numérique indique que l’autorité de certification pense que la clé publique contenue dans le certificat appartient véritablement au principal identifié par le certificat.

Et comment faire confiance à l’autorité de certification ? Étant donné que l’autorité de certification contient un certificat X. 509 qui a été signé par une autorité de certification de niveau supérieur. Cette chaîne de signatures de certificat se poursuit jusqu’à ce qu’elle atteigne une autorité de certification racine, qui est une autorité de certification qui signe ses propres certificats. Si vous faites confiance à l’intégrité de l’autorité de certification racine d’un certificat, vous devez être en mesure de faire confiance à l’authenticité du certificat. Par conséquent, le choix des autorités de certification racine que vous êtes prêt à approuver est un droit important pour un administrateur système.

### <a name="client-certificates"></a>Certificats clients

Lors de la première apparition des protocoles de couche de transport de sécurité, leur objectif principal était de garantir qu’un client se connectait à un serveur authentique et contribue à protéger la confidentialité des données pendant leur transit. Toutefois, SSL 3,0 et TLS 1,0 incluent également la prise en charge de la transmission du certificat d’un client pendant la négociation du protocole. Cette fonctionnalité facultative permet l’authentification mutuelle du client et du serveur.

La décision d’utiliser un certificat client doit être prise dans le contexte de l’application. Les certificats clients ne sont pas nécessaires si la condition principale consiste à authentifier le serveur. Toutefois, si l’authentification du client est essentielle, le certificat d’un client peut être utilisé au lieu de s’appuyer sur l’authentification personnalisée au sein de l’application. L’utilisation de certificats clients est préférable à l’authentification personnalisée, car elle fournit aux utilisateurs un scénario d’authentification unique.

## <a name="using-tls-in-com"></a>Utilisation de TLS dans COM

TLS prend en charge uniquement le niveau d’emprunt d’identité emprunter l’identité (emprunt d’identité du \_ \_ \_ niveau d’IMP RPC \_ ). Si COM négocie TLS en tant que service d’authentification sur un proxy, COM définit le niveau d’emprunt d’identité sur emprunter l’identité, quelle que soit la valeur par défaut du processus. Pour que l’emprunt d’identité fonctionne correctement dans TLS, le client doit fournir un certificat X. 509 au serveur et le serveur doit avoir ce certificat mappé à un compte d’utilisateur particulier sur le serveur. Pour plus d’informations, consultez le [Guide pas à pas de mappage des certificats aux comptes d’utilisateur](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).

TLS ne prend pas en charge le [masquage](cloaking.md). Si un indicateur de masquage et un TLS sont spécifiés dans un appel [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) , E \_ INVALIDARG est retourné.

TLS ne fonctionne pas avec le niveau d’authentification défini sur aucun. Le protocole de transfert entre le client et le serveur examine le niveau d’authentification défini par chaque et choisit le paramètre de sécurité plus élevé pour la connexion.

Les paramètres de sécurité pour TLS peuvent être définis en appelant [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket). Les sections suivantes décrivent les nuances impliquées dans l’exécution de ces appels.

### <a name="how-a-server-sets-the-security-blanket"></a>Comment un serveur définit la couverture de sécurité

Si un serveur souhaite utiliser TLS, il doit spécifier Schannel (RPC \_ C \_ Authn \_ GSS \_ Schannel) comme service d’authentification dans le paramètre *asAuthSvc* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Pour empêcher les clients de se connecter au serveur à l’aide d’un service d’authentification moins sécurisé, le serveur doit spécifier uniquement Schannel comme service d’authentification lorsqu’il appelle **CoInitializeSecurity**. Le serveur ne peut pas modifier la couverture de sécurité après avoir appelé **CoInitializeSecurity**.

Pour utiliser TLS, les paramètres suivants doivent être spécifiés lorsqu’un serveur appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *pVoid* doit être un pointeur vers un objet [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ou un pointeur vers un [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor). Elle ne doit pas être **null** ou un pointeur vers une AppID.
-   *cAuthSvc* ne peut pas avoir la valeur 0 ou-1. Les serveurs COM ne sélectionnent jamais Schannel quand *cAuthSvc* est-1.
-   *asAuthSvc* doit spécifier Schannel comme service d’authentification possible. Pour ce faire, définissez les paramètres [**de \_ \_ service d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) suivants pour le membre Schannel de la [**seule \_ \_ liste d’authentification**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):
    -   *dwAuthnSvc* doit être RPC \_ C \_ Authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* doit avoir la valeur RPC \_ C \_ auth \_ aucun. Actuellement, il est ignoré.
    -   *pPrincipalName* doit être un pointeur vers un [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), casté en un pointeur vers OLECHAR, qui représente le certificat X. 509 du serveur.
-   *dwAuthnLevel* indique le niveau d’authentification minimal qui sera accepté par les clients pour une connexion réussie. Il ne peut pas s’agir du \_ niveau d’authentification RPC C \_ \_ \_ None.
-   *dwCapabilities* ne doit pas avoir l' \_ indicateur EOAC AppID défini. L' \_ \_ indicateur de contrôle d’accès EOAC doit être défini si *pVoid* pointe vers un objet [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ; il ne doit pas être défini si *pVoid* pointe vers un \_ descripteur de sécurité. Pour les autres indicateurs qui peuvent être définis, consultez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Pour plus d’informations sur l’utilisation de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consultez Définition de la [sécurité échelle avec CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-sets-the-security-blanket"></a>Comment un client définit la couverture de sécurité

Si un client souhaite utiliser TLS, il doit spécifier Schannel (RPC \_ C \_ Authn \_ GSS \_ Schannel) dans sa liste de services d’authentification dans le paramètre *pAuthList* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si Schannel n’est pas spécifié comme un service d’authentification possible lorsque la fonction **CoInitializeSecurity** est appelée, un appel ultérieur à [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (ou [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) échouera s’il tente de spécifier Schannel comme service d’authentification.

Les paramètres suivants doivent être spécifiés lorsqu’un client appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):

-   *dwAuthnLevel* spécifie le niveau d’authentification par défaut que le client souhaite utiliser. Il ne peut pas s’agir du \_ niveau d’authentification RPC C \_ \_ \_ None.
-   *dwImpLevel* doit être l' \_ emprunt d’identité RPC C \_ IMP \_ \_ .
-   *pAuthList* doit avoir les [**seuls paramètres \_ d' \_ informations d’authentification**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) suivants en tant que membre de la liste :
    -   *dwAuthnSvc* doit être RPC \_ C \_ Authn \_ GSS \_ Schannel.
    -   *dwAuthzSvc* doit avoir la valeur RPC \_ C \_ auth \_ aucun.
    -   *pAuthInfo* est un pointeur vers un [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), casté en un pointeur vers void, qui représente le certificat X. 509 du client. Si le client n’a pas de certificat ou s’il ne souhaite pas présenter son certificat au serveur, *pAuthInfo* doit avoir la **valeur null** et une connexion anonyme sera tentée avec le serveur.
-   *dwCapabilities* est un ensemble d’indicateurs qui indiquent des fonctionnalités supplémentaires du client. Consultez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour plus d’informations sur les indicateurs à définir.

Pour plus d’informations sur l’utilisation de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), consultez Définition de la [sécurité échelle avec CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

### <a name="how-a-client-changes-the-security-blanket"></a>Modification de la couverture de sécurité par un client

Si un client souhaite utiliser TLS mais modifier la couverture de sécurité après avoir appelé [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), il doit appeler [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) ou [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) avec des paramètres similaires à ceux utilisés dans l’appel à **CoInitializeSecurity**, avec les différences suivantes :

-   *pServerPrincName* indique le nom principal du serveur, au format msstd ou fullsic. Pour plus d’informations sur ces formats, consultez [noms principaux](/windows/desktop/Rpc/principal-names). Si le client possède le certificat X. 509 du serveur, il peut trouver le nom principal en appelant [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).
-   *pAuthInfo* est un pointeur vers un [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), casté en un pointeur vers un \_ handle d’identité d’authentification RPC \_ \_ , qui représente le certificat X. 509 du client. Si le client n’a pas de certificat ou s’il ne souhaite pas présenter son certificat au serveur, *pAuthInfo* doit avoir la **valeur null** et une connexion anonyme sera tentée avec le serveur.
-   *dwCapabilities* se compose d’indicateurs qui indiquent des fonctionnalités supplémentaires du client. Seuls quatre indicateurs peuvent être utilisés pour modifier les paramètres de couverture de sécurité : EOAC \_ par défaut, EOAC \_ \_ l’authentification mutuelle, EOAC \_ n’importe quelle \_ autorité (cet indicateur est déconseillé) et EOAC \_ rendre \_ FULLSIC. Pour plus d’informations, consultez [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Pour plus d’informations sur l’utilisation de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), consultez [définition de la sécurité au niveau du proxy de l’interface](setting-security-at-the-interface-proxy-level.md).

### <a name="example-client-changes-the-security-blanket"></a>Exemple : le client modifie la couverture de sécurité

L’exemple suivant montre comment un client peut modifier la couverture de sécurité pour s’adapter à une demande du serveur pour que le client fournisse son certificat X. 509. Le code de gestion des erreurs est omis par souci de concision.


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Packages COM et de sécurité](com-and-security-packages.md)
</dt> </dl>

 

 