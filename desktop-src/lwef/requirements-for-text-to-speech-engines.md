---
title: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
description: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462258"
---
# <a name="requirements-for-text-to-speech-engines"></a>Configuration requise pour les moteurs de conversion de texte par synthèse vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le moteur doit être entièrement conforme à SAPI 4,0. En outre, le moteur doit également prendre en charge les interfaces SAPI suivantes pour les notifications de signets et de texte avec balises. Ces interfaces permettent à Microsoft Agent d’adapter la sortie du texte à la bulle d’un caractère et au lèvre de synchroniser la bouche du personnage (ou l’équivalent) avec les mots prononcés.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




