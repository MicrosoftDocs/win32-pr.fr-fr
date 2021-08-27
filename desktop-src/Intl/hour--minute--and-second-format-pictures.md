---
description: Cette rubrique décrit les types de format pour les chaînes utilisées pour composer l’image de format d’une chaîne d’heure. Chaque image de format se compose d’une combinaison d’une chaîne de chacun des types de format.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Images de format heure, minute et seconde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e201e72e4da621334a46f20c47e1dd5f731d7ea443bb9970ce07bb7f4e5455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130389"
---
# <a name="hour-minute-and-second-format-pictures"></a>Images de format heure, minute et seconde

Cette rubrique décrit les types de format pour les chaînes utilisées pour composer l’image de format d’une chaîne d’heure. Chaque image de format se compose d’une combinaison d’une chaîne de chacun des types de format.

> [!Note]  
> Dans les types de format, les lettres « m », « s » et « t » doivent être en minuscules, et la lettre « h » doit être en minuscules pour indiquer l’heure sur 12 heures ou en majuscules (« H ») pour indiquer l’heure sur 24 heures.

Les guillemets simples peuvent être utilisés pour marquer les caractères qui doivent être affichés exactement comme spécifiés. Si l’application doit afficher un guillemet simple, elle doit placer deux guillemets simples dans une ligne. Par exemple, « ABC » « bar » est affiché sous la forme « abc’bar ».

Le tableau suivant définit les types de format utilisés pour représenter les heures.

| String | Signification                                                             |
|--------|---------------------------------------------------------------------|
| h      | Heures sans zéros non significatifs pour les heures à un chiffre (horloge de 12 heures). |
| hh     | Heures avec des zéros non significatifs pour les heures à un chiffre (horloge de 12 heures).    |
| H      | Heures sans zéros non significatifs pour les heures à un chiffre (24 heures). |
| HH     | Heures avec des zéros non significatifs pour les heures à un chiffre (24 heures).    |

Le tableau suivant définit les types de format utilisés pour représenter les minutes.

| String | Signification                                                 |
|--------|---------------------------------------------------------|
| m      | Minutes sans zéros non significatifs pour les minutes à un chiffre. |
| MM     | Minutes avec des zéros non significatifs pour les minutes à un chiffre.    |

Le tableau suivant définit les types de format utilisés pour représenter les secondes.

| String | Signification                                                 |
|--------|---------------------------------------------------------|
| s      | Secondes sans zéros non significatifs pour les secondes à un chiffre. |
| ss     | Secondes avec des zéros non significatifs pour les secondes à un chiffre.    |

Le tableau suivant définit les types de format utilisés pour représenter un marqueur d’heure.

| String | Signification|
| ---    | ---    |
| t      | Chaîne de marqueur d’heure à un seul caractère.<br />**Remarque :** Ce format n’est pas recommandé pour une utilisation avec certaines langues, telles que le japonais (Japon). Avec ce format, une application prend toujours le premier caractère de la chaîne du marqueur d’heure, définie par [LOCALE_S1159](locale-s1159.md) (AM) et [LOCALE_S2359](locale-s2359.md) (PM). Pour cette raison, l’application peut créer une mise en forme incorrecte avec la même chaîne utilisée pour AM et PM.|
| tt     | Chaîne de marqueur d’heure à plusieurs caractères. |
