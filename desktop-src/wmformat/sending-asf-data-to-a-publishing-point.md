---
title: Envoi de données ASF à un point de publication
description: Envoi de données ASF à un point de publication
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK, envoyer des données ASF
- Windows Media Format SDK, points de publication
- ASF (Advanced Systems Format), envoi de données
- ASF (format des systèmes avancés), envoyer des données
- ASF (Advanced Systems Format), points de publication
- ASF (format des systèmes avancés), points de publication
- points de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f70c1a49ea7ff6272d0eef9f1a51ff79ec216ed9af445c3078d59dd19841dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197538"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Envoi de données ASF à un point de publication

vous pouvez utiliser le kit de développement logiciel (SDK) de Format multimédia Windows pour envoyer des données ASF à un point de publication sur un serveur multimédia Windows. Le serveur diffuse ensuite les données à partir de ce point de publication. Ce scénario est utile si vous capturez ou ré-encodez du contenu sur un ordinateur et que vous souhaitez distribuer le contenu à partir d’un autre ordinateur (ou de plusieurs ordinateurs). cela est également utile si vous devez déplacer le contenu d’un ordinateur situé à l’intérieur d’un pare-feu vers un serveur de média Windows en dehors du pare-feu, car la distribution push utilise le protocole HTTP.

> [!Note]  
> Un *point de publication* agit essentiellement comme un redirecteur. Le client spécifie le point de publication dans l’URL (par exemple, mms://MyServer/MyPublishingPoint) et le serveur convertit ce point en requête de contenu.

 

Pour envoyer des données au point de publication, attachez l’objet récepteur Push à l’objet Writer. Le récepteur push est utilisé pour ouvrir la connexion au serveur et gérer la session push. L’objet writer gère tous les autres aspects de la création du fichier.

Effectuez les étapes suivantes :

1.  Créez l’objet writer en appelant la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , qui retourne un pointeur [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .
2.  Créez l’objet récepteur Push en appelant la fonction [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , qui retourne un pointeur [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .
3.  Attachez le récepteur réseau au writer en appelant [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sur le writer, avec un pointeur vers l’interface **IWMWriterPushSink** du récepteur réseau.
4.  Connecter au serveur en appelant [**IWMWriterPushSink :: Connecter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Écrire le flux. Cette étape implique la définition du profil sur l’objet Writer, l’envoi d’exemples au writer, et éventuellement d’autres tâches. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md). Des tâches supplémentaires peuvent inclure la définition des attributs de métadonnées (comme décrit dans [utilisation de métadonnées](working-with-metadata.md)) ou la définition de la gestion des droits numériques (DRM) sur le flux (comme décrit dans activation de la [prise en charge de DRM](enabling-drm-support.md)). Ces tâches sont exécutées exactement telles qu’elles sont pour l’écriture de fichiers ASF.
6.  Une fois que vous avez terminé d’écrire, appelez [**IWMWriterAdvanced :: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sur le writer pour détacher l’objet récepteur push.
7.  Appelez [**IWMWriterPushSink :: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) sur le récepteur de notifications push pour mettre fin à la session avec le serveur.

Ces étapes sont illustrées dans l’exemple d’application WMVNetWrite.

> [!Note]  
> Si vous envoyez un fichier vidéo uniquement à faible débit, il est possible qu’il ne démarre pas sur le point de publication pendant plusieurs secondes. Cela peut se produire dans différents cas, par exemple lorsqu’un paquet contient de nombreuses petites images vidéo et pas de son, ou lorsqu’il y a un laps de temps important entre le premier paquet et le deuxième paquet dans un fichier vidéo uniquement à faible débit. Pour éviter ce problème, insérez un flux audio silencieux dans le fichier.

 

## <a name="authentication"></a>Authentification

L’authentification auprès du serveur est gérée automatiquement par l’objet récepteur push. Toutefois, l’application peut avoir besoin de fournir des informations d’identification. Pour cela, vous avez besoin de l’interface de rappel **IWMCredentialCallback** , comme suit :

1.  Implémentez l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) et [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) dans votre application.
2.  Interrogez l’objet récepteur Push pour l’interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .
3.  Appelez [**IWMRegisterCallback :: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) avec un pointeur vers l’interface **IWMStatusCallback** de votre application.
4.  Si le récepteur Push doit obtenir des informations d’identification à partir de l’application, il interroge le pointeur **IWMStatusCallback** pour l’interface **IWMCredentialCallback** et appelle [**IWMCredentialCallback :: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Pour plus d’informations sur cette méthode, consultez [authentification](authentication.md).
5.  Lorsque vous avez terminé, appelez [**IWMRegisterCallback :: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) pour cesser d’obtenir des notifications d’événements à partir du récepteur push.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Envoi de données ASF sur un réseau**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> <dt>

[**Objet récepteur push de l’enregistreur**](writer-push-sink-object.md)
</dt> </dl>

 

 




