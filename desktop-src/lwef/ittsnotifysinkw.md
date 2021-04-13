---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381579"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le moteur doit appeler [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)et [**Visual**](https://www.bing.com/search?q=**Visual**). Le rappel **visuel** doit fournir des phonèmes de la Loi. (Alphabet \[ phonétique international \] La Loi sur la Loi est une notation universelle pour décrire le contenu phonétique de la communication orale. Tous les phonèmes parlants ont des représentations dans la Loi sur la Loi. Pour plus d’informations sur la Loi, consultez la section Spécification de l’API Microsoft Speech \[ du kit de développement logiciel (SDK) speech 4,0 \] à l’adresse [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)

Bien que la notification [**visuelle**](https://www.bing.com/search?q=**Visual**) soit assez riche, Microsoft Agent utilise uniquement la valeur **cIPAPhoneme** pour animer la bouche à mesure que le caractère parle. Tout moteur compatible avec Microsoft Agent doit fournir un flux de notifications **visuelles** étroitement synchronisé reflétant le contenu phonétique de l’énoncé généré. Dans ce cas, la « notification relativement opportune » n’est pas appropriée, car les conférenciers sont assez sensibles aux différences entre la position de la bouche et le contenu acoustique. Les notifications **visuelles** doivent être retournées rapidement.

 

 




