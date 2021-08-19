---
description: Chaîne de l’agent utilisateur
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Chaîne de l’agent utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a4d918845fe317ef64569cde7ef79c7bb1461bcd0205a5ef74daf55b2c0186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328693"
---
# <a name="user-agent-string"></a>Chaîne de l’agent utilisateur

La *chaîne de l’agent utilisateur* contient des informations sur l’identité d’un navigateur. La chaîne de l’agent utilisateur est signalée au serveur Web en tant qu’en-tête HTTP chaque fois qu’un navigateur envoie une demande à un serveur Web. Vous pouvez également y accéder par le biais d’un script côté client. par exemple, vous pouvez afficher la chaîne de l’Agent utilisateur en tapant l’URL suivante dans la barre d’adresse Windows Internet Explorer 8 : « javascript : alert (navigator. userAgent) ». l’illustration suivante montre la boîte de dialogue résultante standard d’Internet Explorer 8 s’exécutant sur Windows 7.

![capture d’écran de la boîte de diaog d’Internet Explorer qui contient la chaîne de l’agent utilisateur](images/useragent-alert.png)

En règle générale, la chaîne de l’agent utilisateur est analysée spécifiquement pour la sous-chaîne MSIE. Selon la version signalée du navigateur, la logique de programmation côté client ou côté serveur effectue une action différente. pour plus d’informations sur la chaîne de l’Agent utilisateur, voir [qu’est-ce qui Windows Internet Explorer reporting comme chaîne User-Agent ?](/previous-versions/cc817582(v=msdn.10)) dans MSDN Library.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



