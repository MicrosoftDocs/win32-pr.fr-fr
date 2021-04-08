---
title: Gestion des erreurs d’application serveur
description: Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671437"
---
# <a name="handling-server-application-errors"></a>Gestion des erreurs d’application serveur

Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200. Si l’application ne retourne pas 200, le client BITS utilise le code d’erreur pour déterminer si l’erreur est une erreur temporaire ou une erreur irrécupérable.

Tous les codes d’erreur 3xx sont des erreurs temporaires, à l’exception de 300-305 et 307, qui sont des erreurs irrécupérables. Tous les codes d’erreur 4xx sont des erreurs irrécupérables, à l’exception de 408 et 409, qui sont des erreurs temporaires. Tous les codes d’erreur 5xx sont des erreurs temporaires, à l’exception de 501 et 505, qui sont des erreurs irrécupérables. Tous les autres codes HTTP sont considérés comme des erreurs temporaires. Notez qu’un code d’erreur 403 est le seul code d’erreur qui empêche les BITS de publier le fichier de téléchargement vers l’application serveur.

Pour récupérer l’erreur, appelez la méthode [**IBackgroundCopyError :: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . Le contexte d’erreur est l' \_ \_ \_ application distante du contexte d’erreur BG \_ .

 

 




