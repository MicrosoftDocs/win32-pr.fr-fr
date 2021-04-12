---
description: Résolveur source
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Résolveur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318729"
---
# <a name="source-resolver"></a>Résolveur source

Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets. Pour créer des sources multimédias dans des applications, la méthode la plus courante est de recourir à un résolveur de source.

En interne, le programme de résolution source utilise des objets *gestionnaires* :

-   Les *gestionnaires de schéma* prennent une URL et créent une source multimédia ou un flux d’octets.
-   Les *gestionnaires de flux d’octets* prennent un flux d’octets et créent une source de média.

Vous pouvez implémenter un gestionnaire personnalisé et l’ajouter au registre. Les gestionnaires de modèles sont inscrits par le schéma d’URL, et les gestionnaires de flux d’octets sont inscrits par l’extension de nom de fichier ou le type MIME.

Cette rubrique contient les sections suivantes :

-   [Utilisation du programme de résolution source](using-the-source-resolver.md)
-   [Configuration d’une source de média](configuring-a-media-source.md)
-   [Gestionnaires de schémas et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> </dl>

 

 



