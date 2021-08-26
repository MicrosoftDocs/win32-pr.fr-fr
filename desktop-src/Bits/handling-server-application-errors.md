---
title: Gestion des erreurs d’application serveur
description: Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005279"
---
# <a name="handling-server-application-errors"></a>Gestion des erreurs d’application serveur

Si l’application serveur traite correctement le fichier téléchargé, l’application doit retourner 200. Si l’application ne retourne pas 200, le client BITS utilise le code d’erreur pour déterminer si l’erreur est une erreur temporaire ou une erreur irrécupérable.

Tous les codes d’erreur 3xx sont des erreurs temporaires, à l’exception de 300-305 et 307, qui sont des erreurs irrécupérables. Tous les codes d’erreur 4xx sont des erreurs irrécupérables, à l’exception de 408 et 409, qui sont des erreurs temporaires. Tous les codes d’erreur 5xx sont des erreurs temporaires, à l’exception de 501 et 505, qui sont des erreurs irrécupérables. Tous les autres codes HTTP sont considérés comme des erreurs temporaires. Notez qu’un code d’erreur 403 est le seul code d’erreur qui empêche les BITS de publier le fichier de téléchargement vers l’application serveur.

Pour récupérer l’erreur, appelez la méthode [**IBackgroundCopyError :: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) . Le contexte d’erreur est l' \_ \_ \_ application distante du contexte d’erreur BG \_ .

 

 




