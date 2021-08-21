---
description: Cette rubrique décrit le contenu vidéo&\# 8211 ; fonctionnalités de protection qu’un pilote Graphics peut fournir.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based protection du contenu avec la vidéo D3D11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ad4301de238ed19fbb047972a15c4acb9e48be069668882fe339ac3da390b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879145"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based protection du contenu avec la vidéo D3D11

Cette rubrique décrit les fonctionnalités de protection du contenu vidéo qu’un pilote Graphics peut fournir.

-   [Introduction](#introduction)
-   [Vue d’ensemble du processus de décodage](#overview-of-the-decoding-process)
-   [Chiffrement de mémoires tampons vidéo compressées pour le décodeur](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. interroger les fonctionnalités protection du contenu du pilote](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurer le canal authentifié](#2-configure-the-authenticated-channel)
    -   [3. configurer la session de chiffrement](#3-configure-the-cryptographic-session)
    -   [4. associer le décodeur à la session de chiffrement](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Envoi de commandes de canal authentifié](#sending-authenticated-channel-commands)
-   [Envoi de requêtes de canal authentifié](#sending-authenticated-channel-queries)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le diagramme suivant montre une vue simplifiée de la façon dont le contenu de la vidéo protégée transite par le pipeline pour être rendu.

![diagramme qui affiche le contenu vidéo protégé.](images/d3d9video01.png)

> [!Note]
>
> Le [chemin d’accès au média protégé](protected-media-path.md) (PMP) n’est pas représenté dans ce diagramme. Le workflow illustré ici peut se produire dans un processus PMP ou dans un processus d’application.

 

Le décodeur reçoit des données vidéo chiffrées et compressées à partir d’une source externe. Il est supposé également que le décodeur reçoit également une clé de chiffrement pour déchiffrer ces données. Cette rubrique ne décrit pas l’échange de clés entre la source et le décodeur vidéo, mais le PMP définit un mécanisme possible. Le GPU n’est pas impliqué à ce niveau.

Pour le décodage à accélération matérielle, le décodeur logiciel transmet le contenu vidéo compressé au GPU. Pour protéger ce contenu, le décodeur rechiffre les données, généralement en utilisant AES-CTR, avant de les transmettre à l’accélérateur matériel. Un mécanisme d’échange de clés est défini entre le décodeur et le pilote Graphics.

Les trames vidéo décodées sont stockées dans la mémoire vidéo, généralement en clair. À ce stade, les trames sont traitées et présentées. Il existe deux options principales pour la présentation.

-   Lorsque vous utilisez l’API D3D9, vous pouvez présenter des frames à l’aide d’une superposition matérielle. Le matériel n’est pas pris en charge dans D3D11. Pour plus d’informations, consultez [prise en charge de la superposition matérielle](hardware-overlay-support.md).
-   Les frames peuvent être présentés par la gestion de la fenêtre du Bureau (DWM) à l’aide d’une surface partagée.

La dernière étape consiste à afficher le cadre sur le moniteur, ce qui peut nécessiter une protection de liaison entre la carte graphique et le périphérique d’affichage. Un exemple de protection de liaison est High-Bandwidth la protection du contenu numérique (HDCP). La protection de liaison est configurée à l’aide de la protection de [sortie](output-protection-manager.md) (OPM). Cette rubrique ne décrit pas OPM ; Pour plus d’informations, consultez [utilisation de Output Protection Manager](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Vue d’ensemble du processus de décodage

Lors du décodage accéléré par le matériel, le décodeur logiciel doit transmettre les données vidéo compressées à la carte graphique. Pour le contenu Premium, ces données doivent généralement être chiffrées, à l’aide d’un chiffrement à clé symétrique, avant d’être envoyées au GPU.

Pour chiffrer la vidéo en vue du décodage, le décodeur logiciel utilise les interfaces suivantes :

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Représente l’appareil décodeur, également appelé accélérateur.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Représente une session de chiffrement, qui fournit la clé de chiffrement.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Représente un canal authentifié qui permet au décodeur logiciel d’associer la session de chiffrement au décodeur.

![diagramme qui montre les interfaces de décodage Direct3D9.](images/d3d9video02.png)

Toutes ces interfaces sont obtenues à partir de l’appareil Direct3D11, comme suit :



| Interface                                                        | Création                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Appelez [**ID3D11VideoDevice :: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). Le type de décodeur est identifié par un GUID de profil. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Appelez [**ID3D11VideoDevice :: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Appelez [**ID3D11VideoDevice :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).                                             |



 

> [!Note]  
> Pour obtenir un pointeur vers l’interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) , appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .

 

Le canal authentifié fournit un canal de communication approuvé entre le décodeur logiciel et le pilote. Le canal de communication fonctionne comme suit :

-   Le pilote fournit une chaîne de certificat X. 509 dont le certificat racine est signé par Microsoft.
-   Le certificat contient une clé publique RSA pour le pilote.
-   Le décodeur logiciel utilise la clé publique pour envoyer au pilote une clé de session AES 128 bits.
-   Le décodeur logiciel envoie des requêtes et des commandes au canal authentifié.
-   La clé de session est utilisée pour calculer les codes d’authentification de message (Mac) pour les requêtes et les commandes. Le pilote utilise les Mac pour vérifier l’intégrité des données de requête/commande, et le décodeur logiciel les utilise pour vérifier l’intégrité des données de réponse du pilote.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Chiffrement de mémoires tampons vidéo compressées pour le décodeur

Voici une vue d’ensemble de haut niveau du processus de chiffrement et de décodage :

1.  Le décodeur logiciel reçoit un flux de données chiffrées à partir de la source vidéo. Le décodeur déchiffre ce flux.
2.  Le décodeur logiciel négocie une clé de session avec la session de chiffrement.
3.  Le décodeur logiciel utilise le canal authentifié pour associer la session de chiffrement à l’appareil de décodage.
4.  Le décodeur logiciel place des données compressées dans des mémoires tampons qu’il obtient à partir de l’appareil de décodage (Accélérateur). Pour le contenu protégé, l’encodeur logiciel chiffre les données qui sont placées dans les tampons, à l’aide de la clé de session du chiffrement.
    > [!Note]  
    > Certains pilotes utilisent une clé de contenu, au lieu de la clé de session, pour le chiffrement. La clé de contenu peut passer d’une image à l’autre.

     

5.  Le décodeur envoie les mémoires tampons compressées chiffrées à l’accélérateur. Pour AES-CTR, le décodeur passe également le vecteur d’initialisation. Si une clé de contenu est utilisée, le décodeur passe la clé de contenu, chiffrée à l’aide de la clé de session.

Direct3D11 offre une prise en charge standard de l’AES-CTR 128 bits, mais est conçu pour s’étendre à des types de chiffrement supplémentaires.

Les cinq sections suivantes fournissent des instructions plus détaillées.

-   [1. interroger les fonctionnalités protection du contenu du pilote](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurer le canal authentifié](#2-configure-the-authenticated-channel)
-   [3. configurer la session de chiffrement](#3-configure-the-cryptographic-session)
-   [4. associer le décodeur à la session de chiffrement](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. interroger les fonctionnalités protection du contenu du pilote

Avant de tenter d’appliquer le chiffrement, procurez-vous les fonctionnalités de protection du contenu du pilote.

1.  Obtient un pointeur vers l’interface ID3D11Device.
2.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
3.  Appelez [**ID3D11VideoDevice :: GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Cette méthode remplit une structure [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) avec les fonctionnalités de protection du contenu du pilote.

En particulier, recherchez les fonctionnalités suivantes :

-   Si le membre **Caps** contient l’indicateur **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** ou **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** , le pilote peut effectuer le chiffrement.
-   Si le membre **Caps** contient l’indicateur **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** , le pilote utilise une clé de contenu distincte pour le déchiffrement.
-   Appelez [**ID3D11VideoDevice :: CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) pour déterminer les types d’échange de clés pris en charge par le pilote pour la génération de la clé de session.

Les fonctionnalités supplémentaires sont indiquées dans le membre **Caps** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurer le canal authentifié

L’étape suivante consiste à configurer le canal authentifié.

1.  Appelez [**ID3D11VideoDevice :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) pour créer le canal authentifié. Pour le paramètre *ChannelType* , spécifiez un type de canal qui correspond aux fonctionnalités du pilote.
    -   Le type de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** correspond à **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   Le type de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** correspond à **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    La méthode **CreateAuthenticatedChannel** retourne un pointeur vers l’interface [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) .
2.  Appelez [**ID3D11AuthenticatedChannel :: GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) pour connaître la taille du certificat X. 509 du pilote. Allouez une mémoire tampon de la taille requise.
3.  Appelez [**ID3D11AuthenticatedChannel :: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) pour récupérer le certificat. La méthode copie le certificat dans la mémoire tampon qui a été allouée à l’étape précédente.
4.  Vérifiez que le certificat du pilote a été signé par Microsoft et qu’il n’a pas été révoqué.
5.  Récupérez la clé publique à partir du certificat.
6.  Générez une clé de session RSA aléatoire. Cette clé de session est utilisée pour signer les données envoyées au canal authentifié. Chiffrez la clé de session à l’aide de la clé publique du pilote.
7.  Appelez [**ID3D11VideoContext :: NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) pour envoyer la clé de session chiffrée au pilote.
8.  Initialisez le canal sécurisé comme suit :
    1.  Remplissez une structure [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) comme décrit dans la documentation.
    2.  Envoyez la commande [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) en appelant [**ID3D11VideoContext :: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) comme décrit dans la section [envoi de commandes de canal authentifié](#sending-authenticated-channel-commands). Cette commande contient les numéros de séquence de départ pour les commandes et les requêtes qui sont envoyées au canal authentifié.
9.  Vérifiez le type de canal en envoyant une requête [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) au canal authentifié, comme décrit dans la section [envoi de requêtes de canal authentifié](#sending-authenticated-channel-queries). Vérifiez que le type de canal correspond à ce que vous avez spécifié dans la méthode [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurer la session de chiffrement

Ensuite, configurez la session de chiffrement et établissez la clé de session.

1.  Appelez [**ID3D11VideoDevice :: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) pour créer la session de chiffrement. Cette méthode retourne un pointeur vers l’interface [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) .
2.  Appelez [**ID3D11CryptoSession :: GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) pour connaître la taille du certificat X. 509 du pilote. Allouez une mémoire tampon de la taille requise.
3.  Appelez [**ID3D11CryptoSession :: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) pour récupérer le certificat. La méthode copie le certificat dans la mémoire tampon qui a été allouée à l’étape précédente.
4.  Vérifiez que le certificat du pilote a été signé par Microsoft et qu’il n’a pas été révoqué.
5.  Récupérez la clé publique à partir du certificat.
6.  Générez une clé de session RSA aléatoire. Il s’agit d’une clé de session distincte de la clé de session du canal authentifié. Chiffrez la clé de session à l’aide de la clé publique du pilote.
7.  Appelez [**ID3D11VideoContext :: NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) pour envoyer la clé de session chiffrée au pilote.
8.  Si les fonctionnalités de protection du contenu incluent **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, créez une clé de contenu RSA aléatoire. Ce sera utilisé ultérieurement dans le processus de décodage.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. associer le décodeur à la session de chiffrement

Ensuite, associez l’appareil du décodeur à l’appareil Direct3D11 et à la session de chiffrement, comme suit :

1.  Obtenir un descripteur de l’appareil Direct3D11, en envoyant une requête [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) au canal authentifié.
2.  Remplissez une structure [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) avec les informations suivantes :
    -   Définissez le membre **DecodeHandle** sur le handle retourné par [**ID3D11VideoDecoder :: GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).
    -   Définissez le membre **CryptoSessionHandle** sur le handle retourné par [**ID3D11CryptoSession :: GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).
    -   Définissez le membre **DeviceHandle** sur le descripteur de l’appareil Direct3D11.
3.  Appelez [**ID3D11VideoContext :: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) pour envoyer une commande [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) au canal authentifié.

Le diagramme suivant illustre l’échange de handles :

![diagramme qui montre comment le décodeur DXVA est associé à la session de chiffrement.](images/d3d9video03.png)

Le décodeur logiciel peut désormais utiliser la clé de session de chiffrement pour chiffrer les mémoires tampons vidéo compressées. Chaque mémoire tampon compressée aura son propre vecteur d’initialisation (IV) spécifié dans le membre **pIV** de la structure [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) .

## <a name="sending-authenticated-channel-commands"></a>Envoi de commandes de canal authentifié

Un ensemble de commandes est défini pour la configuration du canal authentifié et la définition de diverses protections de contenu. Pour obtenir la liste des commandes, consultez [protection du contenu des commandes](content-protection-commands.md).

Pour envoyer une commande au canal authentifié, procédez comme suit.

1.  Renseignez la structure des données d’entrée. Cette structure de données est toujours une structure [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) suivie de champs supplémentaires. Renseignez la structure **D3D11_AUTHENTICATED_CONFIGURE_INPUT** comme indiqué dans le tableau suivant.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membre</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>omac</strong></td>
    <td>Ignorez ce champ pour l’instant.</td>
    </tr>
    <tr class="even">
    <td><strong>ConfigureType</strong></td>
    <td>GUID qui identifie la commande. Pour obtenir la liste des commandes, consultez <a href="content-protection-commands.md">protection du contenu des commandes</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>hChannel</strong></td>
    <td>Handle du canal authentifié.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>Numéro séquentiel. Le premier numéro de séquence est spécifié par l’envoi d’une commande <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Chaque fois que vous envoyez une autre commande, incrémentez ce nombre de 1. Le numéro de séquence protège contre les attaques par relecture.
    <blockquote>
    [!Note]<br />
Deux numéros de séquence distincts sont utilisés, un pour les commandes et un pour les requêtes.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure d’entrée. Copiez ensuite cette valeur de balise dans le membre **OMAC** .
3.  Appelez [**ID3D11VideoContext :: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel).
4.  Le pilote place la sortie de la commande dans la structure [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) .
5.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure de sortie. Comparez ceci avec la valeur du membre **OMAC** . Échouent s’ils ne correspondent pas.
6.  Comparez les valeurs des membres **ConfigureType**, **hChannel** et de la structure de sortie à vos valeurs pour **ces membres.** Échouent s’ils ne correspondent pas.
7.  Incrémentez le numéro de séquence de la commande suivante.

## <a name="sending-authenticated-channel-queries"></a>Envoi de requêtes de canal authentifié

Un ensemble de requêtes est défini pour la récupération d’informations sur le canal authentifié. Pour obtenir la liste des requêtes, consultez [protection du contenu des requêtes](content-protection-queries.md).

Pour envoyer une commande au canal authentifié, procédez comme suit.

1.  Renseignez la structure des données d’entrée. Cette structure de données est toujours une structure [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) , éventuellement suivie de champs supplémentaires. Renseignez la structure **D3D11_AUTHENTICATED_QUERY_INPUT** comme indiqué dans le tableau suivant.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membre</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Affectée</strong></td>
    <td>GUID qui identifie la requête. Pour obtenir la liste des requêtes, consultez <a href="content-protection-queries.md">protection du contenu des requêtes</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>hChannel</strong></td>
    <td>Handle du canal authentifié.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>Numéro séquentiel. Le premier numéro de séquence est spécifié par l’envoi d’une commande <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Chaque fois que vous envoyez une autre requête, incrémentez ce nombre de 1. Le numéro de séquence protège contre les attaques par relecture.
    <blockquote>
    [!Note]<br />
Deux numéros de séquence distincts sont utilisés, un pour les commandes et un pour les requêtes.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Appelez [**ID3D11VideoContext :: QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel).
3.  Le pilote place la sortie de la requête dans une structure [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) . Cette structure est suivie de champs supplémentaires, selon le type de requête.
4.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure de sortie. Comparez ceci avec la valeur du membre **OMAC** . Échouent s’ils ne correspondent pas.
5.  Comparez les valeurs des membres **ConfigureType**, **hChannel** et de la structure de sortie à vos valeurs pour **ces membres.** Échouent s’ils ne correspondent pas.
6.  Incrémentez le numéro de séquence de la requête suivante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 
