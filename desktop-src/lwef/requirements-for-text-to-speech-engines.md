---
title: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
description: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746414"
---
# <a name="requirements-for-text-to-speech-engines"></a>Configuration requise pour les moteurs de conversion de texte par synthèse vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le moteur doit être entièrement conforme à SAPI 4,0. En outre, le moteur doit également prendre en charge les interfaces SAPI suivantes pour les notifications de signets et de texte avec balises. Ces interfaces permettent à Microsoft Agent d’adapter la sortie du texte à la bulle d’un caractère et au lèvre de synchroniser la bouche du personnage (ou l’équivalent) avec les mots prononcés.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




