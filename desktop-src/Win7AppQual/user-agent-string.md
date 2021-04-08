---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Chaîne de l’agent utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953237"
---
# <a name="user-agent-string"></a>Chaîne de l’agent utilisateur

La *chaîne de l’agent utilisateur* contient des informations sur l’identité d’un navigateur. La chaîne de l’agent utilisateur est signalée au serveur Web en tant qu’en-tête HTTP chaque fois qu’un navigateur envoie une demande à un serveur Web. Vous pouvez également y accéder par le biais d’un script côté client. Par exemple, vous pouvez afficher la chaîne de l’agent utilisateur en tapant l’URL suivante dans la barre d’adresses Windows Internet Explorer 8 : « JavaScript : Alert (Navigator. userAgent) ». L’illustration suivante montre la boîte de dialogue résultante standard d’Internet Explorer 8 s’exécutant sur Windows 7.

![capture d’écran de la boîte de diaog d’Internet Explorer qui contient la chaîne de l’agent utilisateur](images/useragent-alert.png)

En règle générale, la chaîne de l’agent utilisateur est analysée spécifiquement pour la sous-chaîne MSIE. Selon la version signalée du navigateur, la logique de programmation côté client ou côté serveur effectue une action différente. Pour plus d’informations sur la chaîne de l’agent utilisateur, voir [qu’est-ce que Windows Internet Explorer signalera comme chaîne de User-Agent ?](/previous-versions/cc817582(v=msdn.10)) dans MSDN Library.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



