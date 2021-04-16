---
title: Configuration HTTP requise pour les téléchargements BITS
description: BITS prend en charge les téléchargements HTTP et HTTPs, ainsi que les chargements et requiert que le serveur prenne en charge le protocole HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462070"
---
# <a name="http-requirements-for-bits-downloads"></a>Configuration HTTP requise pour les téléchargements BITS

BITS prend en charge les téléchargements HTTP et HTTPs, ainsi que les chargements et requiert que le serveur prenne en charge le protocole HTTP/1.1. Pour les téléchargements, la méthode **Head** du serveur http doit retourner la taille du fichier et sa méthode d' **extraction** doit prendre en charge les en-têtes Content-Range et Content-Length. Par conséquent, BITS transfère uniquement le contenu du fichier statique et génère une erreur si vous tentez de transférer du contenu dynamique, à moins que le script ASP, ISAPI ou CGI ne prenne en charge les en-têtes Content-Range et Content-Length.

BITS peut utiliser un serveur HTTP/1.0, à condition qu’il réponde aux exigences de la méthode **Head** et de la méthode d' **extraction** .

Pour prendre en charge le téléchargement des plages d’un fichier, le serveur doit prendre en charge les exigences suivantes :

-   Autorisez les en-têtes MIME à inclure les en-têtes standard content-Range et Content-type, plus un maximum de 180 octets d’autres en-têtes.
-   Autorisez un maximum de deux CR/LFs entre les en-têtes HTTP et la première chaîne de limite.

 

 




