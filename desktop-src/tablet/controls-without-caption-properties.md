---
description: Introduction à l’utilisation de contrôles sans propriétés de légende pour Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Contrôles sans propriétés de légende
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5cd8eb0c87f946d8540fb63d75408dcf98a880cefcd1ba295ba2ba113e6828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774109"
---
# <a name="controls-without-caption-properties"></a>Contrôles sans propriétés de légende

Lorsqu’un contrôle n’a pas sa propre propriété Caption, effectuez les étapes suivantes pour garantir que les aides à l’accessibilité peuvent identifier les contrôles :

-   Créez un contrôle de texte statique avec un nom explicite et descriptif.
-   Placez l’étiquette statique de manière à ce qu’elle précède immédiatement le contrôle référencé, dans l’ordre de tabulation.
-   assurez-vous que le texte de l’étiquette se termine par un signe deux-points, par exemple, « Paramètres : »
-   Placez le texte de l’étiquette immédiatement à gauche ou avant le contrôle référencé.
-   Rendez le texte statique invisible s’il n’est pas approprié de l’afficher visuellement. Pour ce faire, affectez l’attribut approprié dans le script de ressources. Cela peut être approprié lorsque le nom ou la fonction d’un contrôle est fourni visuellement par d’autres moyens que le contrôle de texte statique, tel qu’un graphique ou une case d’option associée.

L’utilisation correcte des contrôles statiques est la seule façon d’implémenter correctement les clés d’accès soulignées pour les contrôles qui n’ont pas d’étiquette intrinsèque. Pour plus d’informations sur l’utilisation de contrôles qui n’ont pas de propriétés de légende, consultez la section [accessibilité](/windows/desktop/accessibility) .

 

 
