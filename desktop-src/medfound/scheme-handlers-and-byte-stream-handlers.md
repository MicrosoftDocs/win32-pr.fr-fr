---
description: Cette rubrique décrit les détails internes de la façon dont le programme de résolution source crée une source de média.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Gestionnaires de schémas et gestionnaires de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5cbb2ee0af93e456e86b6eab16ff44705f5380
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531653"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Gestionnaires de schémas et gestionnaires de Byte-Stream

Cette rubrique décrit les détails internes de la façon dont le programme de résolution source crée une source de média. Lisez cette rubrique si vous implémentez une source de média personnalisée pour Media Foundation, et que vous souhaitez que la source du média soit disponible pour les applications via le programme de résolution source.

Le programme de résolution source peut créer une source de média à partir d’une URL ou d’un flux d’octets (autrement dit, un pointeur [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ). Pour ce faire, il utilise des objets d’assistance appelés *gestionnaires*. Pour les URL, le programme de résolution source utilise des *gestionnaires de schémas*. Pour les flux d’octets, elle utilise des *gestionnaires de flux d’octets*.

Un gestionnaire de schéma prend une URL comme entrée et crée une source de média ou un flux d’octets. Si elle crée un flux d’octets, le programme de résolution source le transmet à un gestionnaire de flux d’octets, qui crée la source du média. L’illustration suivante montre ce processus.

![Diagramme montrant le processus de résolution source](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Gestionnaires de schéma

Les gestionnaires de schéma sont utilisés quand l’application appelle [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou son équivalent asynchrone [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

Le programme de résolution source recherche les gestionnaires de schéma dans le registre. Les gestionnaires de modèles sont répertoriés par schéma d’URL, sous les clés suivantes :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

où *&lt; Scheme &gt;* est le schéma d’URL que le gestionnaire est conçu pour analyser. Le schéma comprend le caractère «  : » de fin ; par exemple, « http : ».

Pour inscrire un nouveau gestionnaire de schéma, ajoutez une entrée dont le nom est le CLSID du gestionnaire de schémas, sous forme de chaîne canonique : `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . La valeur de l’entrée est une chaîne (REG \_ SZ) contenant une brève description du gestionnaire, telle que « mon gestionnaire de schémas ». La partie importante de l’entrée est le CLSID. Le programme de résolution source crée le gestionnaire en appelant **CoCreateInstance** avec ce CLSID.

Les gestionnaires de schéma exposent l’interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . Si le programme de résolution source trouve un gestionnaire de schéma qui correspond au schéma d’URL, le programme de résolution source appelle [**IMFSchemeHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), en passant l’URL d’origine. Le gestionnaire de schéma ouvre l’URL et tente d’analyser le contenu. À ce stade, le gestionnaire de schéma a deux options :

-   Créez une source de média.
-   Créez un flux d’octets.

Si elle crée une source de média, le programme de résolution source retourne la source du média à l’application. Si elle crée un flux d’octets, le programme de résolution source tente de trouver un gestionnaire de flux d’octets approprié, comme décrit dans la section suivante.

## <a name="byte-stream-handlers"></a>Gestionnaires de Byte-Stream

Les gestionnaires de flux d’octets sont utilisés quand l’application appelle [**IMFSourceResolver :: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) ou son équivalent asynchrone [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream). Ils sont également utilisés lorsqu’un gestionnaire de schéma retourne un flux d’octets, comme décrit précédemment.

Comme avec les gestionnaires de modèles, les gestionnaires de flux d’octets sont répertoriés dans le registre. Elles sont répertoriées par extension de nom de fichier ou type MIME (ou les deux), sous les clés suivantes :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

où *&lt; ExtensionOrMimeType &gt;* est l’extension de nom de fichier ou le type MIME. Les extensions de fichier incluent le caractère'. 'initial ; par exemple, « . wmv ».

L’extension de nom de fichier fait partie de l’URL, fournie par l’application. Le type MIME peut être disponible via l’attribut de [**\_ \_ \_ type de contenu BYTESTREAM MF**](mf-bytestream-content-type-attribute.md) sur le flux d’octets.

Pour inscrire un nouveau gestionnaire de flux d’octets, ajoutez une entrée dont le nom est le CLSID du gestionnaire, sous forme de chaîne canonique. La valeur de l’entrée est une chaîne (REG \_ SZ) contenant une brève description du gestionnaire, telle que « mon gestionnaire de Byte-Stream ». Le programme de résolution source appelle **CoCreateInstance** pour créer le gestionnaire à partir du CLSID. Vous pouvez inscrire le même gestionnaire sous plusieurs extensions ou types MIME.

Les gestionnaires de flux d’octets exposent l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Si le programme de résolution source trouve un gestionnaire de flux d’octets correspondant, il appelle [**IMFByteStreamHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). L’entrée de cette méthode est un pointeur vers le flux d’octets, plus l’URL d’origine, si elle est disponible. Le gestionnaire de flux d’octets lit à partir du flux d’octets jusqu’à ce qu’il analyse suffisamment de données pour créer la source du média.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 



