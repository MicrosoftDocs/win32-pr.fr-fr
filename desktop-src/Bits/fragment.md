---
title: Fragment
description: Utilisez le paquet fragment pour envoyer un fragment du fichier de téléchargement au serveur.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BITS de fragment
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101281"
---
# <a name="fragment"></a>Fragment

Utilisez le paquet **fragment** pour envoyer un fragment du fichier de téléchargement au serveur.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a>headers

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits
</dt> <dd>

Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.

Remplacez l’URL distante par l’URI absolu ou relatif. Remplacez généralement l’URL distante par le nom de fichier distant du travail. Pour les considérations relatives à l’équilibrage de la charge réseau, consultez l’en-tête BITS-Host-ID dans le paquet [**Create-session**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type
</dt> <dd>

Identifie ce paquet de requête en tant que paquet de fragments.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>ID de session BITS
</dt> <dd>

GUID de chaîne qui identifie la session sur le serveur. Remplacez {GUID} par l’identificateur de session que le serveur renvoie dans le paquet [**d’accusé de réception de la réponse de création de session**](ack-for-create-session.md) .

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name
</dt> <dd>

Spécifiez cet en-tête uniquement avec le fragment initial. Remplacez filename par le nom du fichier local du travail. Le nom n’inclut pas le chemin d’accès.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length
</dt> <dd>

Remplacez length par le nombre d’octets envoyés dans le corps du fragment.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Plage de contenu
</dt> <dd>

Indique au serveur où appliquer la plage dans le fichier de destination. Remplacez la plage par les décalages de début et de fin de la plage dans le fichier de destination. Les décalages sont de base zéro. Si la plage donnée chevauche une plage existante, BITS écrit uniquement la partie sans chevauchement de la plage ; Le service BITS ne remplace pas le contenu existant. Par exemple, si le premier paquet contient la plage comprise entre 0 et 100 et que le deuxième paquet contenait la plage 50 à 150, BITS écrit uniquement les octets 101 à 150 du deuxième paquet. Remplacez total-length par le nombre total d’octets dans le fichier.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding
</dt> <dd>

Remplacez encodage par le type d’encodage utilisé par le client sur le fragment. Le client doit utiliser l’encodage identifié par le serveur dans l’en-tête Accept-Encoding de l’accusé de réception pour le paquet de réponse [**de création de session**](ack-for-create-session.md) . Le serveur utilise le type d’encodage pour décoder le fragment. Tous les fragments doivent spécifier le même encodage.

N’envoyez pas cet en-tête si le type d’encodage est Identity. Le serveur BITS prend en charge uniquement l’encodage d’identité.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fragment est une plage d’octets envoyés dans le corps du paquet. Le client envoie les fragments dans l’ordre séquentiel, en commençant par le décalage zéro ; le serveur n’effectue pas le suivi des plages non contiguës. Si le client envoie des plages non contiguës, le serveur renvoie un code de retour HTTP 416 (satisfaisante) dans l' [**accusé de réception de**](ack-for-fragment.md) la réponse du fragment.

Les en-têtes Content-*xxxx* sont des en-têtes HTTP 1,1 standard. Pour plus d’informations sur les en-têtes Content-*xxxx* , consultez la spécification [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACK pour fragment**](ack-for-fragment.md)
</dt> <dt>

[**Fermer-session**](close-session.md)
</dt> <dt>

[**Créer une session**](create-session.md)
</dt> </dl>

 

 




