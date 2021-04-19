---
description: Uniscribe enregistre les mappages Unicode-à-glyphe (CMAP), les largeurs de glyphe et les tables de mise en forme de script OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Mise en cache (internationalisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf8bf7dd10fe414bc170086ff9b8c34142dc197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522251"
---
# <a name="caching-internationalization"></a>Mise en cache (internationalisation)

Uniscribe enregistre les mappages Unicode-à-glyphe (CMAP), les largeurs de glyphe et les tables de mise en forme de script OpenType. Un handle vers les tables pour une police particulière d’une taille particulière est appelé « cache de script ». De nombreuses fonctions Uniscribe appellent à la fois pour un paramètre de handle de contexte de périphérique et un pointeur vers une structure de [**\_ cache de script**](script-cache.md) . Ces fonctions recherchent d’abord des informations dans le cache de script, à l’aide du contexte de périphérique uniquement lorsque les tables requises ne sont pas déjà mises en cache. Lors de l’appel de la fonction [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)ou [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , l’application doit passer un pointeur vers une structure de **\_ cache de script** . Le descripteur doit être initialisé à la **valeur null** avant la première fois que l’application le transmet à une fonction Uniscribe. L’application ne doit jamais passer le même handle pour différentes polices ou tailles différentes.

Une application peut libérer un cache de script à tout moment. Uniscribe conserve les décomptes de références dans ses caches de police et de former, libère les données de police uniquement lorsque toutes les tailles de la police sont libérées et libère les données de l’adapteur uniquement lorsque toutes les polices prises en charge par le formateur sont libérées. Lorsque l’application est effectuée avec un style, elle doit appeler la fonction [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) pour libérer le cache de script du style.

Pour [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) et [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), l’application doit passer un contexte de périphérique null. Le plus souvent, l’appel est concluant, car les tables requises sont déjà mises en cache. Si la mise en forme ou le placement requiert l’accès à un contexte de périphérique, **ScriptShape** ou **ScriptPlace** retourne immédiatement avec le \_ code d’erreur E en attente. L’application doit ensuite sélectionner la police dans le contexte de périphérique. Pour la plupart des applications, cela permet d’obtenir des performances en évitant la préparation répétée d’un handle de contexte d’appareil avec des appels à [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
