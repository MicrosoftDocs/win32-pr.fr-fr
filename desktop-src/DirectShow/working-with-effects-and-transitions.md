---
description: Utilisation des effets et des transitions
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Utilisation des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953184"
---
# <a name="working-with-effects-and-transitions"></a>Utilisation des effets et des transitions

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Les effets modifient une seule séquence, piste ou composition. Les transitions créent des seques à partir d’une piste ou d’un compositionsto.

Les [services d’édition DirectShow](directshow-editing-services.md) utilisent des objets de transformation DirectX pour ses transitions vidéo et leurs effets vidéo. Pour les transitions vidéo, utilisez n’importe quel objet de transformation DirectX à deux entrées 2D. Pour les effets vidéo, utilisez n’importe quel objet de transformation DirectX à un entrée en 2D. Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers. Toutefois, plusieurs sont fournis avec DirectShow et d’autres sont fournis avec Microsoft Internet Explorer. Pour plus d’informations sur les transitions fournies avec Internet Explorer, consultez informations de référence sur les [filtres visuels et les transitions](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).

Pour les effets audio, vous pouvez utiliser n’importe quel filtre d’effet audio DirectShow. DES fournit également un [effet d’enveloppe de volume](volume-envelope-effect.md) pour la définition du volume sur une piste ou un clip. DES ne prend pas en charge les transitions audio.

Cette section contient les rubriques suivantes :

-   [Ajout d’objets Effect et transition](adding-effect-and-transition-objects.md)
-   [Aperçu des effets et des transitions](previewing-effects-and-transitions.md)
-   [Énumération des effets et des transitions](enumerating-effects-and-transitions.md)
-   [Définition des propriétés des effets et des transitions](setting-properties-on-effects-and-transitions.md)
-   [Sens de la transition](transition-direction.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
