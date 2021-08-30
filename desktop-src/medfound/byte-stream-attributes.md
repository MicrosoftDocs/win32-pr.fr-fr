---
description: Attributs de flux d’octets
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Attributs de flux d’octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc6b6a73d58b3b5817f6c5654a4968c3f4677c0dca9ad4d184e93ee82d8206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959369"
---
# <a name="byte-stream-attributes"></a>Attributs de flux d’octets

Les attributs suivants s’appliquent à certains flux d’octets. Pour déterminer si un flux d’octets prend en charge les attributs, interrogez l’objet de flux d’octets pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Attribut                                                                                  | Description                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**\_type de \_ contenu \_ BYTESTREAM MF**](mf-bytestream-content-type-attribute.md)              | Spécifie le type MIME d’un flux d’octets.                         |
| [**\_durée BYTESTREAM \_ MF**](mf-bytestream-duration-attribute.md)                       | Spécifie la durée d’un flux d’octets, en unités de 100 nanosecondes. |
| [\_URI du \_ \_ fichier IFO BYTESTREAM MF \_](mf-bytestream-ifo-file-uri.md)                           | Spécifie l’URL d’un fichier IFO associé.                      |
| [**\_heure de \_ dernière \_ modification de BYTESTREAM \_ MF**](mf-bytestream-last-modified-time-attribute.md) | Spécifie la date de la dernière modification d’un flux d’octets.                   |
| [**\_nom d' \_ origine MF BYTESTREAM \_**](mf-bytestream-origin-name-attribute.md)                | Spécifie l’URL d’origine d’un flux d’octets.                     |



 

Les attributs suivants s’appliquent aux gestionnaires de flux d’octets.



| Attribut                                                                                    | Description                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ accepte \_ l' \_ écriture de partage](mf-bytestreamhandler-accepts-share-write.md) | Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



