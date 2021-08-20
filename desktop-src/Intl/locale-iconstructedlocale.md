---
description: Paramètres régionaux \_ ICONSTRUCTEDLOCALE Description de la constante
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 26d54ce55393f54d56f521231e257a8b0692758f8e6c830a890d81c8f82e8422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809637"
---
# <a name="locale_iconstructedlocale"></a>paramètres régionaux \_ ICONSTRUCTEDLOCALE

Identificateur à demander si les paramètres régionaux sont des paramètres régionaux « construits ». L’utilisation de ce LCTYPE est déconseillée.

cela identifie les paramètres régionaux pour lesquels Windows nombre n’ont pas d’informations complètes et doit « construire » des informations au moment de l’exécution. en général, les informations fournies par LOCALE_ICONSTRUCTEDLOCALE sont limitées en ce qui concerne Windows fournira autant de données que possible pour chaque paramètre régional. Par conséquent, l’utilisation de ce LCTYPE est déconseillée.


| Valeur | Signification                 |
|-------|-------------------------|
| 0     | Non construit         |
| 1     | Est un paramètre régional construit |


Par exemple, une demande pour « fr-fr » ou l’allemand dans le États-Unis. NLS utilise les données en langue allemande qu’il peut trouver et les données de la région États-Unis qu’il peut trouver. 

Cela peut ne pas être parfait, par exemple, le système n’aura probablement pas d’informations sur le nom de États-Unis en allemand. Toutefois, si l’application ou l’utilisateur désire un contexte de « -US », les données retournées sont les meilleures disponibles. 

Les applications qui utilisent LOCALE_ICONSTRUCTEDLOCALE pour refuser des paramètres régionaux et revenir à des paramètres régionaux différents finissent par être moins expérimentés, comme le débarquement de-fr ou fr-US dans cet exemple. Aucun de ces n’est proche de la demande d’origine de la langue allemande avec une région de États-Unis.

