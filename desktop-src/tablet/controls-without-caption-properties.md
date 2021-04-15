---
description: Introduction à l’utilisation de contrôles sans propriétés de légende pour Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Contrôles sans propriétés de légende
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524380"
---
# <a name="controls-without-caption-properties"></a>Contrôles sans propriétés de légende

Lorsqu’un contrôle n’a pas sa propre propriété Caption, effectuez les étapes suivantes pour garantir que les aides à l’accessibilité peuvent identifier les contrôles :

-   Créez un contrôle de texte statique avec un nom explicite et descriptif.
-   Placez l’étiquette statique de manière à ce qu’elle précède immédiatement le contrôle référencé, dans l’ordre de tabulation.
-   Assurez-vous que le texte de l’étiquette se termine par un signe deux-points, par exemple, « paramètres : »
-   Placez le texte de l’étiquette immédiatement à gauche ou avant le contrôle référencé.
-   Rendez le texte statique invisible s’il n’est pas approprié de l’afficher visuellement. Pour ce faire, affectez l’attribut approprié dans le script de ressources. Cela peut être approprié lorsque le nom ou la fonction d’un contrôle est fourni visuellement par d’autres moyens que le contrôle de texte statique, tel qu’un graphique ou une case d’option associée.

L’utilisation correcte des contrôles statiques est la seule façon d’implémenter correctement les clés d’accès soulignées pour les contrôles qui n’ont pas d’étiquette intrinsèque. Pour plus d’informations sur l’utilisation de contrôles qui n’ont pas de propriétés de légende, consultez la section [accessibilité](/windows/desktop/accessibility) .

 

 
