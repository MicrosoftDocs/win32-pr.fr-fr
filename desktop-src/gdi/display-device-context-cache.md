---
description: Le système gère un cache de l’affichage des contextes de périphérique qu’il utilise pour les contextes de périphérique communs, parents et de fenêtre.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Afficher le cache du contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96bbf8cb388e31e43a0eacf9200b638fe8a232749dd5e2ef8ab67318b30d9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062429"
---
# <a name="display-device-context-cache"></a>Afficher le cache du contexte de périphérique

Le système gère un cache de l’affichage des contextes de périphérique qu’il utilise pour les contextes de périphérique communs, parents et de fenêtre. Le système récupère un contexte de périphérique (Device Context) à partir du cache chaque fois qu’une application appelle la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . le système retourne le contrôleur de réseau dans le cache lorsque l’application appelle ensuite la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ou [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Il n’existe aucune limite prédéterminée sur la quantité de contextes de périphérique qu’un cache peut contenir ; le système crée un contexte de périphérique d’affichage pour le cache si aucun n’est disponible. Dans ce contexte, une application peut avoir plus de cinq contextes de périphérique actifs du cache à la fois. Toutefois, l’application doit continuer à libérer ces contextes de périphérique après utilisation. Étant donné que de nouveaux contextes de périphérique d’affichage pour le cache sont alloués dans l’espace du tas de l’application, le fait de ne pas libérer les contextes de périphérique finit par consommer tout l’espace disponible du tas. Le système indique cet échec en renvoyant une erreur lorsqu’il ne peut pas allouer de l’espace pour le nouveau contexte de périphérique. D’autres fonctions non liées au cache peuvent également renvoyer des erreurs.

 

 



