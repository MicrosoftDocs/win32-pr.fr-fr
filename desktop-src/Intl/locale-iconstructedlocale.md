---
description: Paramètres régionaux \_ ICONSTRUCTEDLOCALE Description de la constante
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106541569"
---
# <a name="locale_iconstructedlocale"></a>paramètres régionaux \_ ICONSTRUCTEDLOCALE

Identificateur à demander si les paramètres régionaux sont des paramètres régionaux « construits ». L’utilisation de ce LCTYPE est déconseillée.

Cela identifie les paramètres régionaux pour lesquels Windows n’ont pas d’informations complètes et qui doivent « construire » des informations au moment de l’exécution. En général, les informations fournies par LOCALE_ICONSTRUCTEDLOCALE sont limitées, car Windows fournira autant de données que possible pour chaque paramètre régional. Par conséquent, l’utilisation de ce LCTYPE est déconseillée.


| Valeur | Signification                 |
|-------|-------------------------|
| 0     | Non construit         |
| 1     | Est un paramètre régional construit |


Par exemple, une demande pour « fr-fr » ou l’allemand dans le États-Unis. NLS utilise les données en langue allemande qu’il peut trouver et les données de la région États-Unis qu’il peut trouver. 

Cela peut ne pas être parfait, par exemple, le système n’aura probablement pas d’informations sur le nom de États-Unis en allemand. Toutefois, si l’application ou l’utilisateur désire un contexte de « -US », les données retournées sont les meilleures disponibles. 

Les applications qui utilisent LOCALE_ICONSTRUCTEDLOCALE pour refuser des paramètres régionaux et revenir à des paramètres régionaux différents finissent par être moins expérimentés, comme le débarquement de-fr ou fr-US dans cet exemple. Aucun de ces n’est proche de la demande d’origine de la langue allemande avec une région de États-Unis.

