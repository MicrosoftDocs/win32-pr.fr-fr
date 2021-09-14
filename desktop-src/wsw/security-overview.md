---
title: Vue d’ensemble de la sécurité
description: l’infrastructure de sécurité de Windows API de Services Web (WWSAPI) assure l’intégrité des messages, la confidentialité, la détection de relecture et l’authentification du serveur à l’aide de la sécurité de transport.
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- Vue d’ensemble de la sécurité services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295803"
---
# <a name="security-overview"></a>Vue d’ensemble de la sécurité

l’infrastructure de sécurité de Windows API des Services Web (WWSAPI) fournit les éléments suivants :

-   Intégrité des messages, confidentialité, détection de relecture et authentification du serveur à l’aide de la sécurité de transport.
-   Authentification du client, telle que la validation des jetons de sécurité, les vérifications de l’approbation et de la révocation des certificats, etc., en utilisant la sécurité de message ou de transport SOAP.

## <a name="the-security-programming-model"></a>Le modèle de programmation de sécurité

La sécurité est associée aux [canaux de communication](channel-layer-overview.md). La sécurisation d’un canal comprend les étapes suivantes.

-   Créez et initialisez une ou plusieurs [**liaisons de sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) appropriées pour les exigences de sécurité de l’application.
-   Créez une [**Description de sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contenant ces liaisons de sécurité.
-   Créez un [**canal**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) ou un [**proxy de service**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (côté client) ou créez un [**écouteur**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) ou un [**hôte de service**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (côté serveur) en transmettant cette description de sécurité.
-   Effectuez les étapes de programmation normale des canaux de l’ouverture, de l’acceptation, de l’envoi, de la réception, de la fermeture, etc.

Les messages envoyés et reçus sur le canal sont sécurisés automatiquement par le runtime conformément à la description de sécurité fournie. Si vous le souhaitez, vous pouvez affiner ces étapes en spécifiant un ou plusieurs paramètres de sécurité à l' [ensemble du canal](security-channel-settings.md) dans les paramètres de sécurité de la description de la sécurité ou de la [liaison](security-binding-settings.md) dans une liaison de sécurité.

Toute autorisation requise des identités d’expéditeur doit être effectuée par l’application à l’aide des [résultats de traitement de sécurité](security-processing-results.md) joints à chaque message reçu. Les étapes d’autorisation ne sont pas spécifiées dans la description de sécurité, et ne sont pas exécutées automatiquement par le Runtime.

Les erreurs dans la description de sécurité, telles que les liaisons non prises en charge, les propriétés/champs non applicables, l’absence de propriétés/champs requis ou les valeurs de propriété/champ non valides, entraînent l’échec de la création du canal ou de l’écouteur.

## <a name="selecting-security-bindings"></a>Sélection des liaisons de sécurité

Lors de la conception de la sécurité d’une application, la décision principale est la sélection des liaisons de sécurité à inclure dans la description de la sécurité. Voici quelques recommandations pour choisir des liaisons de sécurité adaptées au scénario de sécurité d’une application. une méthode heuristique utile consiste tout d’abord à comprendre quels types d’informations d’identification de sécurité (tels que les [**certificats X. 509**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential), [**Windows nom d’utilisateur/mot de passe de domaine**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential), [**nom d’utilisateur/mot de passe définis par l’application**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)) seront disponibles pour l’application, puis choisissez une liaison de sécurité qui peut utiliser ce type d’informations d’identification.

-   La sécurité du transport, où la sécurité est appliquée au niveau du flux d’octets de transport (sous les limites de message SOAP), est la première option à prendre en compte.
    -   Pour les scénarios Internet, et pour les scénarios intranet où un certificat X. 509 peut être déployé sur le serveur, l’application peut utiliser la [**\_ liaison de sécurité de \_ transport \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). L’exemple suivant illustre cette option. Client : serveur [HttpClientWithSslExample](httpclientwithsslexample.md) : [HttpServerWithSslExample](httpserverwithsslexample.md).

        Si l’authentification du client via l’authentification d’en-tête HTTP est souhaitée, une [**\_ \_ \_ \_ \_ liaison de sécurité d’en-tête WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) peut être ajoutée pour fournir cette fonctionnalité.

    -   pour les scénarios d’Intranet où Windows des protocoles d’authentification intégrés tels que Kerberos, NTLM et SPNEGO sont appropriés, l’application peut utiliser la [**liaison de sécurité de TRANSPORT de WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding). L’exemple suivant illustre cette option : client : [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server : [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

        Client sur des canaux nommés : [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        Serveur sur les canaux nommés : [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   pour les scénarios d’ordinateur local où Windows des protocoles d’authentification intégrés, tels que Kerberos, NTLM et SPNEGO, est approprié, l’application peut utiliser la [**liaison de sécurité de \_ transport ws TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) ou la liaison de [**\_ \_ sécurité de \_ transport \_ \_ sspi ws NAMEDPIPE**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding). La [**\_ liaison de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) est préférable dans de tels scénarios, car elle garantit que le trafic ne sortira pas de l’ordinateur (il s’agit de la propriété de la **\_ \_ \_ liaison de canal WS NAMEDPIPE**).

-   La sécurité en mode mixte, où la sécurité de transport protège la connexion et un en-tête de WS-Security dans le message SOAP fournit l’authentification du client, est l’option suivante à prendre en compte. Les liaisons suivantes sont utilisées conjointement avec l’une des liaisons de sécurité de transport décrites dans la section précédente.
    -   Lorsque le client est authentifié par une paire nom d’utilisateur/mot de passe au niveau de l’application, l’application peut utiliser une [**\_ liaison de sécurité de \_ message \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) pour fournir les données d’authentification. Les exemples suivants illustrent l’utilisation de cette liaison conjointement avec une [**\_ liaison de \_ \_ sécurité \_ de transport WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding):
        -   Client : [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   Serveur : [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   Lorsque le client est authentifié par un ticket Kerberos, l’application peut utiliser une [**liaison de \_ \_ sécurité de \_ message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) pour fournir les données d’authentification.
    -   Lors de l’utilisation d’un [contexte de sécurité](security-context.md), le client établit d’abord un contexte de sécurité avec le serveur, puis utilise ce contexte pour authentifier les messages. Pour activer cette fonctionnalité, la description de sécurité doit contenir [**une \_ \_ liaison de \_ \_ sécurité de \_ message de contexte de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Une fois la connexion établie, les contextes de sécurité peuvent être transmis par le biais de jetons légers, ce qui évite d’avoir à envoyer les informations d’identification du client potentiellement volumineuses et gourmandes en calculs à chaque message.
    -   Dans un scénario de [sécurité fédérée](federation.md) , le client obtient d’abord un jeton de sécurité émis par un service d’émission de jeton de sécurité (STS), puis présente le jeton émis à un service. Côté client : pour obtenir le jeton de sécurité du STS, l’application peut utiliser [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken). L’application peut également utiliser une bibliothèque de fournisseur de jetons de sécurité côté client comme CardSpace ou LiveID, puis utiliser sa sortie pour créer localement un jeton de sécurité à l’aide de [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). Dans les deux cas, une fois que le jeton de sécurité est disponible pour le client, il peut être présenté au service à l’aide d’une description de sécurité contenant une [**liaison de sécurité de \_ message de \_ jeton \_ \_ \_ WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding). Côté serveur : si le jeton de sécurité émis par le STS est un jeton SAML, le serveur peut utiliser une description de sécurité avec une [**\_ liaison de \_ \_ sécurité \_ de message de WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding).
        > [!Note]  
        > Windows 7 et Windows Server 2008 R2 : WWSAPI prend uniquement en charge [ws-Trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) et [ws-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) comme défini par [Lightweight Web Services Security profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Pour plus d’informations sur l’implémentation de Microsoft, consultez la section relative à la [syntaxe du message](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

         
-   La dernière option à prendre en compte consiste à utiliser des liaisons d’authentification sans utiliser de liaison de protection telle que la [**\_ liaison de sécurité de \_ transport \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Cela entraînera la transmission des informations d’identification en texte clair et peut avoir des implications en matière de sécurité. L’utilisation de cette option doit être évaluée avec soin pour s’assurer qu’il n’existe aucune vulnérabilité. L’échange de messages entre les serveurs principaux sur un réseau privé sécurisé constitue un exemple d’utilisation potentielle. Les configurations suivantes prennent en charge cette option.

    -   [**WS \_ La \_ \_ liaison de \_ sécurité \_ d’authentification d’en-tête http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) prend en charge cette option dans toutes les configurations.
    -   [**WS \_ La \_ \_ \_ liaison de sécurité de message username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) prend en charge cette option sur le serveur lors de l’utilisation de http comme transport.
    -   [**WS \_ La \_ \_ liaison de \_ sécurité \_ des messages Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) prend en charge cette option sur le serveur lors de l’utilisation du protocole http en tant que transport.
    -   [**WS \_ La \_ \_ liaison de \_ sécurité \_ de message de contexte de sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) prend en charge cette option sur le serveur lors de l’utilisation de http comme transport.
    -   [**WS \_ La \_ \_ \_ liaison de sécurité des messages SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) prend en charge cette option sur le serveur lors de l’utilisation de http en tant que transport.

    L’activation de cette option nécessite de définir explicitement le [**\_ \_ niveau de protection WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) sur une valeur autre que le **niveau de \_ protection WS \_ \_ Sign \_ et \_ Encrypt**.

## <a name="channels-and-security"></a>Canaux et sécurité

Comme indiqué ci-dessus, la sécurité est limitée aux canaux. En outre, les opérations de canal correspondent aux étapes de sécurité de manière cohérente sur toutes les liaisons de sécurité.

-   Création de canal : le jeu de liaisons de sécurité spécifié dans la description de sécurité est validé et reste fixe pour le canal par la suite. La forme de la pile de canaux, y compris les canaux secondaires à utiliser pour les négociations WS-Trust, est également déterminée.
-   Canal ouvert : les informations d’identification fournies dans le cadre des liaisons de sécurité sont chargées, et les sessions de sécurité sont établies. En général, un canal ouvert contient un état de sécurité « en direct ». L’ouverture d’un canal client spécifie également l’adresse du point de terminaison du serveur par rapport à laquelle l’authentification du serveur sera effectuée par le Runtime.
-   Entre l’ouverture et la fermeture d’un canal : les messages peuvent être envoyés et reçus en toute sécurité au cours de cette phase.
-   Envoi de messages : les jetons de contexte de sécurité sont obtenus ou renouvelés selon les besoins et la sécurité est appliquée à chaque message transmis en fonction de la description de la sécurité. Les erreurs rencontrées lors de l’application de la sécurité sont retournées à l’application en tant qu’erreurs d’envoi.
-   Réception du message : la sécurité est vérifiée sur chaque message reçu conformément à la description de la sécurité. Toutes les erreurs de vérification de sécurité de message sont renvoyées à l’application en tant qu’erreurs de réception. Ces erreurs par message n’affectent pas l’état du canal ou les réceptions ultérieures. L’application peut ignorer une réception ayant échoué et redémarrer une réception pour un autre message.
-   Abandon du canal : le canal peut être abandonné à tout moment pour arrêter toutes les e/s sur le canal. Lors de l’abandon, le canal passe dans un état d’erreur et n’autorise plus d’envoi ou de réception. Toutefois, le canal peut toujours conserver un état de sécurité « réel », de sorte qu’une fermeture de canal suivante sera nécessaire pour supprimer tous les États correctement.
-   Fermeture du canal : l’état de sécurité créé à l’ouverture est supprimé et les sessions sont détruites. Les jetons de contexte de sécurité sont annulés. La pile de canaux est conservée, mais elle ne contient pas d’état de sécurité « actif » ou d’informations d’identification chargées.
-   Canal libre : la pile de canaux générée au moment de la création, ainsi que toutes les ressources de sécurité, sont libérées.

## <a name="security-apis"></a>API Sécurité

La documentation de l’API pour la sécurité est regroupée dans les rubriques suivantes.

-   [Description de la sécurité](security-description.md)
    -   [Paramètres de canal de sécurité](security-channel-settings.md)
    -   [Liaisons de sécurité](security-bindings.md)
        -   [Informations d'identification de sécurité](security-credentials.md)
        -   [Paramètres de liaison de sécurité](security-binding-settings.md)
-   [Fédération](federation.md)
-   [Contexte de sécurité](security-context.md)
-   [Identité du point de terminaison](endpoint-identity.md)
-   [Résultats du traitement de la sécurité](security-processing-results.md)

## <a name="security"></a>Sécurité

Lors de l’utilisation de l’API de sécurité WWSAPI, les applications font face à plusieurs risques de sécurité :

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>Configuration intempestive accidentelle
</dt> <dd>

WWSAPI prend en charge une gamme d’options de configuration liées à la sécurité. Consultez par exemple [**\_ ID de \_ \_ propriété \_ de liaison WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id). Certaines de ces options, telles que **la \_ propriété de liaison WS Security, \_ \_ \_ autorisent les \_ \_ clients anonymes** à permettre à l’application de réduire le niveau de sécurité par défaut fourni par les différentes liaisons de sécurité. L’utilisation de ces options doit être soigneusement évaluée pour s’assurer qu’il n’existe aucun vecteur d’attaque résultant.

En outre, comme décrit ci-dessus, WWSAPI permet à une application de désactiver délibérément certaines étapes requises pour sécuriser complètement un échange de messages, par exemple autoriser la désactivation du chiffrement, même si les informations d’identification de sécurité sont transmises. Cela est autorisé à activer certains scénarios spécifiques et ne doit pas être utilisé pour la communication générale. Le [**\_ \_ niveau de protection WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) doit être réduit spécifiquement pour permettre ces scénarios, et les applications ne doivent pas modifier cette valeur sauf si cela est absolument nécessaire, ce qui entraîne la désactivation de nombreuses vérifications conçues pour garantir une configuration sécurisée.

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>Stockage des informations confidentielles en mémoire
</dt> <dd>

Les informations confidentielles, telles que les mots de passe, qui sont stockées en mémoire sont susceptibles d’être extraites par un attaquant privilégié au moyen, par exemple, du fichier d’échange. WWSAPI effectue une copie des informations d’identification fournies et chiffre cette copie, en laissant les données d’origine non protégées. L’application est responsable de la protection de l’instance d’origine. En outre, la copie chiffrée est brièvement déchiffrée lors de son utilisation, ouvrant une fenêtre pour l’extraire.

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>Déni de service
</dt> <dd>

Le traitement de la sécurité peut consommer des ressources importantes. Chaque liaison de sécurité supplémentaire augmente ces coûts. WWSAPI abandonne le traitement de la sécurité dès qu’un échec de vérification de sécurité se produit, mais certaines vérifications, telles que les décisions d’autorisation, peuvent ne pas avoir lieu tant que le travail important n’a pas été effectué.

Lors du traitement d’un message sur le serveur, l’état de sécurité est stocké sur le segment de mémoire du message. L’application peut limiter la consommation de mémoire pendant le traitement de la sécurité en réduisant la taille du segment de mémoire par le biais des \_ Propriétés du segment de propriété de message WS \_ \_ \_ . En outre, certaines liaisons de sécurité telles que la \_ liaison de sécurité de message du contexte de sécurité WS \_ \_ \_ \_ peuvent entraîner l’allocation de ressources par le serveur pour le compte du client. Les limites de ces ressources peuvent être configurées par le biais des valeurs d' [**\_ ID de propriété de \_ liaison \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) suivantes :

-   contexte de sécurité de la \_ propriété de liaison WS sécurité- \_ \_ \_ \_ \_ nombre maximal de \_ \_ contextes en attente
-   contexte de sécurité de la \_ propriété de liaison WS Security- \_ \_ \_ \_ \_ nombre maximal de \_ \_ contextes actifs
-   \_intervalle de \_ \_ renouvellement du \_ \_ contexte de \_ sécurité \_ de la propriété de liaison WS Security
-   \_intervalle de \_ \_ substitution du \_ \_ contexte de \_ sécurité \_ de la propriété de liaison WS Security

La définition de ces limites à des valeurs faibles réduit la consommation de mémoire maximale, mais peut entraîner le rejet des clients légitimes lorsque le quota est atteint.

</dd> </dl>

 

 