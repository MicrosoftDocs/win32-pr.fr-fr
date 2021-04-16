---
description: Décrit le contenu vidéo&\# 8211 ; fonctionnalités de protection qu’un pilote Graphics peut fournir.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based protection du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571362"
---
# <a name="gpu-based-content-protection"></a>GPU-Based protection du contenu

Cette rubrique décrit les fonctionnalités de protection du contenu vidéo qu’un pilote Graphics peut fournir.

-   [Introduction](#introduction)
-   [Vue d’ensemble du processus de décodage](#overview-of-the-decoding-process)
-   [Chiffrement de mémoires tampons vidéo compressées pour le décodeur](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. interroger les fonctionnalités protection du contenu du pilote](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurer le canal authentifié](#2-configure-the-authenticated-channel)
    -   [3. configurer la session de chiffrement](#3-configure-the-cryptographic-session)
    -   [4. obtenir un descripteur de l’appareil décodeur DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. associer le décodeur DXVA à la session de chiffrement](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Envoi de commandes de canal authentifié](#sending-authenticated-channel-commands)
-   [Envoi de requêtes de canal authentifié](#sending-authenticated-channel-queries)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le diagramme suivant montre une vue simplifiée de la façon dont le contenu de la vidéo protégée transite par le pipeline pour être rendu.

![diagramme qui affiche le contenu vidéo protégé.](images/d3d9video01.png)

> [!Note]  
> Le [chemin d’accès au média protégé](protected-media-path.md) (PMP) n’est pas représenté dans ce diagramme. Le workflow illustré ici peut se produire dans un processus PMP ou dans un processus d’application.

 

Le décodeur reçoit des données vidéo chiffrées et compressées à partir d’une source externe. Il est supposé également que le décodeur reçoit également une clé de chiffrement pour déchiffrer ces données. Cette rubrique ne décrit pas l’échange de clés entre la source et le décodeur vidéo, mais le PMP définit un mécanisme possible. Le GPU n’est pas impliqué à ce niveau.

Pour le décodage à accélération matérielle, le décodeur logiciel transmet le contenu vidéo compressé au GPU. Pour protéger ce contenu, le décodeur rechiffre les données, généralement en utilisant AES-CTR, avant de les transmettre à l’accélérateur matériel. Un mécanisme d’échange de clés est défini entre le décodeur et le pilote Graphics.

Les trames vidéo décodées sont stockées dans la mémoire vidéo, généralement en clair. À ce stade, les trames sont traitées et présentées. Il existe deux options principales pour la présentation.

-   Les frames peuvent être présentés à l’aide d’une superposition matérielle. Pour plus d’informations, consultez [prise en charge de la superposition matérielle](hardware-overlay-support.md).
-   Les frames peuvent être présentés par la gestion de la fenêtre du Bureau (DWM) à l’aide d’une surface partagée.

La dernière étape consiste à afficher le cadre sur le moniteur, ce qui peut nécessiter une protection de liaison entre la carte graphique et le périphérique d’affichage. Un exemple de protection de liaison est High-Bandwidth la protection du contenu numérique (HDCP). La protection de liaison est configurée à l’aide de la protection de [sortie](output-protection-manager.md) (OPM). Cette rubrique ne décrit pas OPM ; Pour plus d’informations, consultez [utilisation de Output Protection Manager](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Vue d’ensemble du processus de décodage

Lors du décodage accéléré par le matériel, le décodeur logiciel doit transmettre les données vidéo compressées à la carte graphique. Pour le contenu Premium, ces données doivent généralement être chiffrées, à l’aide d’un chiffrement à clé symétrique, avant d’être envoyées au GPU.

Pour chiffrer la vidéo en vue du décodage, le décodeur logiciel utilise les interfaces suivantes :

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Représente l’appareil du décodeur DXVA, également appelé accélérateur.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Représente une session de chiffrement, qui fournit la clé de chiffrement.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Représente un canal authentifié qui permet au décodeur logiciel d’associer la session de chiffrement au décodeur DXVA.

![diagramme qui montre les interfaces de décodage Direct3D9.](images/d3d9video02.png)

Toutes ces interfaces sont obtenues à partir du périphérique Direct3D, comme suit :



| Interface                                                                | Création                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Appelez [**IDirectXVideoDecoderService :: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). L’appareil de décodage DXVA est identifié par un GUID de profil DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Appelez [**IDirect3DDevice9Video :: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Pour obtenir un pointeur vers l’interface [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) , appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un appareil D3D9Ex.

 

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
3.  Le décodeur logiciel utilise le canal authentifié pour associer la session de chiffrement à l’appareil de décodage DXVA.
4.  Le décodeur logiciel place des données compressées dans des mémoires tampons DXVA qu’il obtient à partir de l’appareil de décodage DXVA (Accélérateur). Pour le contenu protégé, l’encodeur logiciel chiffre les données qui sont placées dans les tampons DXVA, à l’aide de la clé de session du chiffrement.
    > [!Note]  
    > Certains pilotes utilisent une clé de contenu, au lieu de la clé de session, pour le chiffrement. La clé de contenu peut passer d’une image à l’autre.

     

5.  Le décodeur envoie les mémoires tampons compressées chiffrées à l’accélérateur. Pour AES-CTR, le décodeur passe également le vecteur d’initialisation. Si une clé de contenu est utilisée, le décodeur transmet la clé de contenu, chiffrée à l’aide de la clé de session.

Direct3D offre une prise en charge standard de l’AES-CTR 128 bits, mais est conçu pour s’étendre à des types de chiffrement supplémentaires.

Les cinq sections suivantes fournissent des instructions plus détaillées.

-   [1. interroger les fonctionnalités protection du contenu du pilote](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurer le canal authentifié](#2-configure-the-authenticated-channel)
-   [3. configurer la session de chiffrement](#3-configure-the-cryptographic-session)
-   [4. obtenir un descripteur de l’appareil décodeur DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. associer le décodeur DXVA à la session de chiffrement](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. interroger les fonctionnalités protection du contenu du pilote

Avant de tenter d’appliquer le chiffrement, procurez-vous les fonctionnalités de protection du contenu du pilote.

1.  Obtenir un pointeur vers l’appareil Direct3D 9.
2.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) .
3.  Appelez [**IDirect3DDevice9Video :: GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Cette méthode remplit une structure [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) avec les fonctionnalités de protection du contenu du pilote.

En particulier, recherchez les fonctionnalités suivantes :

-   Si le membre **Caps** contient l’indicateur **D3DCPCAPS_SOFTWARE** ou **D3DCPCAPS_HARDWARE** , le pilote peut effectuer le chiffrement.
-   Le membre **KeyExchangeType** spécifie comment effectuer l’échange de clés pour la clé de session.
-   Si le membre **Caps** contient l’indicateur **D3DCPCAPS_CONTENTKEY** , le pilote utilise une clé de contenu distincte pour le chiffrement. C’est important lorsque vous générez la clé de session.

Les fonctionnalités supplémentaires sont indiquées dans le membre **Caps** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurer le canal authentifié

L’étape suivante consiste à configurer le canal authentifié.

1.  Appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) pour créer le canal authentifié. Pour le paramètre *ChannelType* , spécifiez un type de canal qui correspond aux fonctionnalités du pilote.
    -   Le type de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** correspond à **D3DCPCAPS_SOFTWARE**.
    -   Le type de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** correspond à **D3DCPCAPS_HARDWARE**.

    La méthode **CreateAuthenticatedChannel** retourne un pointeur vers l’interface [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) , ainsi qu’un handle vers le canal. Le descripteur est utilisé ultérieurement pour associer la session de chiffrement au canal authentifié.
2.  Appelez [**IDirect3DAuthenticatedChannel9 :: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) pour connaître la taille du certificat X. 509 du pilote. Allouez une mémoire tampon de la taille requise.
3.  Appelez [**IDirect3DAuthenticatedChannel9 :: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) pour récupérer le certificat. La méthode copie le certificat dans la mémoire tampon qui a été allouée à l’étape précédente.
4.  Vérifiez que le certificat du pilote a été signé par Microsoft et qu’il n’a pas été révoqué.
5.  Récupérez la clé publique à partir du certificat.
6.  Générez une clé de session RSA aléatoire. Cette clé de session est utilisée pour signer les données envoyées au canal authentifié. Chiffrez la clé de session à l’aide de la clé publique du pilote.
7.  Appelez [**IDirect3DAuthenticatedChannel9 :: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) pour envoyer la clé de session chiffrée au pilote.
8.  Initialisez le canal sécurisé comme suit :
    1.  Remplissez une structure [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) comme décrit dans la documentation.
    2.  Envoyez la commande [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) en appelant [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) comme décrit dans la section [envoi de commandes de canal authentifié](#sending-authenticated-channel-commands). Cette commande contient les numéros de séquence de départ pour les commandes et les requêtes qui sont envoyées au canal authentifié.
9.  Vérifiez le type de canal en envoyant une requête [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) au canal authentifié, comme décrit dans la section [envoi de requêtes de canal authentifié](#sending-authenticated-channel-queries). Vérifiez que le type de canal correspond à ce que vous avez spécifié dans la méthode [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurer la session de chiffrement

Ensuite, configurez la session de chiffrement et établissez la clé de session.

1.  Appelez [**IDirect3DDevice9Video :: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) pour créer la session de chiffrement. Cette méthode retourne un pointeur vers l’interface [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) , ainsi qu’un handle vers la session de chiffrement.
2.  Appelez [**IDirect3DCryptoSession9 :: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) pour connaître la taille du certificat X. 509 du pilote. Allouez une mémoire tampon de la taille requise.
3.  Appelez [**IDirect3DCryptoSession9 :: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) pour récupérer le certificat. La méthode copie le certificat dans la mémoire tampon qui a été allouée à l’étape précédente.
4.  Vérifiez que le certificat du pilote a été signé par Microsoft et qu’il n’a pas été révoqué.
5.  Récupérez la clé publique à partir du certificat.
6.  Générez une clé de session RSA aléatoire. Il s’agit d’une clé de session distincte de la clé de session du canal authentifié. Chiffrez la clé de session à l’aide de la clé publique du pilote.
7.  Appelez [**IDirect3DCryptoSession9 :: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) pour envoyer la clé de session chiffrée au pilote.
8.  Si les fonctionnalités de protection du contenu incluent **D3DCPCAPS_CONTENTKEY**, créez une clé de contenu RSA aléatoire. Ce sera utilisé ultérieurement dans le processus de décodage.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. obtenir un descripteur de l’appareil décodeur DXVA

Pour l’étape suivante, vous aurez besoin d’un handle vers l’appareil décodeur DXVA. Pour obtenir ce handle, remplissez une structure DXVA2_DecodeExecuteParams comme suit :


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Définissez le membre **pExtensionData** de la structure [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) sur l’adresse d’une structure [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) .

Dans la structure [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) , définissez la **fonction** Member sur **DXVA2_DECODE_GET_DRIVER_HANDLE**. Définissez **pPrivateOutputData** sur l’adresse d’une mémoire tampon suffisamment grande pour stocker une valeur de **handle** . (Dans l’exemple précédent, cette mémoire tampon est la variable *hDecodeDeviceHandle* .)

Appelez ensuite [**IDirectXVideoDecoder :: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) et transmettez l’adresse de la structure [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) . Le handle du décodeur DXVA est retourné dans **pPrivateOutputData**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. associer le décodeur DXVA à la session de chiffrement

Ensuite, associez l’appareil de décodage DXVA à l’appareil Direct3D et à la session de chiffrement, comme suit :

1.  Obtenir un descripteur de l’appareil décodeur DXVA, comme décrit dans la section précédente.
2.  Obtenir un handle sur le périphérique Direct3D, en envoyant une requête [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) au canal authentifié.
3.  Remplissez une structure [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) avec les informations suivantes :
    -   Définissez le membre **DXVA2DecodeHandle** sur le descripteur de l’appareil décodeur DXVA.
    -   Définissez le membre **CryptoSessionHandle** sur le descripteur de la session de chiffrement. Ce handle est retourné par la méthode [**IDirect3DDevice9Video :: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) .
    -   Définissez le membre **DeviceHandle** sur le descripteur de périphérique Direct3D.
4.  Appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) pour envoyer une commande [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) au canal authentifié.

Le diagramme suivant illustre l’échange de handles :

![diagramme qui montre comment le décodeur DXVA est associé à la session de chiffrement.](images/d3d9video03.png)

Le décodeur logiciel peut désormais utiliser la clé de session de chiffrement pour chiffrer les mémoires tampons vidéo compressées. Chaque mémoire tampon compressée aura son propre vecteur d’initialisation (IV) spécifié dans le membre **pvPVPState** de la structure [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) .

## <a name="sending-authenticated-channel-commands"></a>Envoi de commandes de canal authentifié

Un ensemble de commandes est défini pour la configuration du canal authentifié et la définition de diverses protections de contenu. Pour obtenir la liste des commandes, consultez [protection du contenu des commandes](content-protection-commands.md).

Pour envoyer une commande au canal authentifié, procédez comme suit.

1.  Renseignez la structure des données d’entrée. Cette structure de données est toujours une structure [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) suivie de champs supplémentaires. Renseignez la structure **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** comme indiqué dans le tableau suivant.

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
    <td>Numéro séquentiel. Le premier numéro de séquence est spécifié par l’envoi d’une commande <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Chaque fois que vous envoyez une autre commande, incrémentez ce nombre de 1. Le numéro de séquence protège contre les attaques par relecture.
    <blockquote>
    [!Note]<br />
Deux numéros de séquence distincts sont utilisés, un pour les commandes et un pour les requêtes.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure d’entrée. Copiez ensuite cette valeur de balise dans le membre **OMAC** .
3.  Appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  Le pilote place la sortie de la commande dans la structure [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) .
5.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure de sortie. Comparez ceci avec la valeur du membre **OMAC** . Échouent s’ils ne correspondent pas.
6.  Comparez les valeurs des membres **ConfigureType**, **hChannel** et de la structure de sortie à vos valeurs pour **ces membres.** Échouent s’ils ne correspondent pas.
7.  Incrémentez le numéro de séquence de la commande suivante.

## <a name="sending-authenticated-channel-queries"></a>Envoi de requêtes de canal authentifié

Un ensemble de requêtes est défini pour la récupération d’informations sur le canal authentifié. Pour obtenir la liste des requêtes, consultez [protection du contenu des requêtes](content-protection-queries.md).

Pour envoyer une commande au canal authentifié, procédez comme suit.

1.  Renseignez la structure des données d’entrée. Cette structure de données est toujours une structure [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) , éventuellement suivie de champs supplémentaires. Renseignez la structure **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** comme indiqué dans le tableau suivant.

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
    <td>Numéro séquentiel. Le premier numéro de séquence est spécifié par l’envoi d’une commande <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Chaque fois que vous envoyez une autre requête, incrémentez ce nombre de 1. Le numéro de séquence protège contre les attaques par relecture.
    <blockquote>
    [!Note]<br />
Deux numéros de séquence distincts sont utilisés, un pour les commandes et un pour les requêtes.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  Le pilote place la sortie de la requête dans une structure [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) . Cette structure est suivie de champs supplémentaires, selon le type de requête.
4.  Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **OMAC** de la structure de sortie. Comparez ceci avec la valeur du membre **OMAC** . Échouent s’ils ne correspondent pas.
5.  Comparez les valeurs des membres **ConfigureType**, **hChannel** et de la structure de sortie à vos valeurs pour **ces membres.** Échouent s’ils ne correspondent pas.
6.  Incrémentez le numéro de séquence de la requête suivante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
