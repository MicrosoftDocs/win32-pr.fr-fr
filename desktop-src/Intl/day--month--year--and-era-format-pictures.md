---
description: L’application utilise les éléments décrits dans cette rubrique pour construire une chaîne d’image de format se terminant par null.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Images de format de jour, de mois, d’année et d’ère
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867934"
---
# <a name="day-month-year-and-era-format-pictures"></a>Images de format de jour, de mois, d’année et d’ère

L’application utilise les éléments décrits dans cette rubrique pour construire une chaîne d’image de format se terminant par null. Si des espaces sont utilisés pour séparer les éléments de la chaîne, ces espaces s’affichent au même emplacement dans la chaîne de sortie.

> [!Note]  
> Les types de format « d », « g » et « y » doivent être en minuscules et la lettre « M » doit être en majuscules.

 

Par exemple, pour obtenir la chaîne de date « Wed, aoû 31 94 », l’application utilise la chaîne d’image « DDD », « MMM JJ AA ».

L’application utilise des guillemets simples pour marquer les caractères à afficher exactement comme spécifié. Si l’application doit afficher un guillemet simple, elle doit placer deux guillemets simples dans une ligne. Par exemple, « ABC » « bar » est affiché sous la forme « abc’bar ».

Le tableau suivant définit les types de format utilisés pour représenter les jours.



| Type de format | Signification                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Jour du mois en chiffres sans zéros non significatifs pour les jours à un chiffre.                                                                                                                                                                                                                                                                                                   |
| jj          | Jour du mois en chiffres avec des zéros non significatifs pour les jours à un chiffre.                                                                                                                                                                                                                                                                                                      |
| ddd         | Jour de la semaine, tel que spécifié par une valeur [ \_ \* SABBREVDAYNAME locale](locale-sabbrev-constants.md) , par exemple, « mon » en anglais (États-Unis).**Windows Vista et versions ultérieures :** si une version abrégée du jour de la semaine est requise, votre application doit utiliser les constantes [ \_ \* SSHORTESTDAYNAME des paramètres régionaux](locale-sshortestdayname-constants.md) .<br/> |
| dddd        | Jour de la semaine spécifié par une valeur de [ \_ SDAYNAME \* de paramètres régionaux](locale-sdayname-constants.md) .                                                                                                                                                                                                                                                                              |



 

Le tableau suivant définit les types de format utilisés pour représenter des mois.



| Type de format | Signification                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Month en chiffres sans zéros non significatifs pour les mois à un seul chiffre.                                                                                                                   |
| MM          | Month en chiffres avec des zéros non significatifs pour les mois à un seul chiffre.                                                                                                                      |
| MMM         | Le mois abrégé tel que spécifié par une valeur [ \_ SABBREVMONTHNAME \* locale](locale-sabbrev-constants.md) , par exemple, « Nov » en anglais (États-Unis).                             |
| MMMM        | Mois comme spécifié par une valeur [ \_ \* SMONTHNAME locale](locale-smonthname-constants.md) , par exemple, « novembre » pour l’anglais (États-Unis) et « noviembre » pour l’espagnol (Espagne). |



 

Le tableau suivant définit les types de format utilisés pour représenter des années.



| Type de format | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Année représentée uniquement par le dernier chiffre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Année représentée uniquement par les deux derniers chiffres. Un zéro non significatif est ajouté pour les années à un seul chiffre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| aaaa        | Année représentée par un entier à quatre ou cinq chiffres, selon le calendrier utilisé. Les calendriers thaï bouddhiste et coréen ont des années à cinq chiffres. Le modèle « yyyy » affiche cinq chiffres pour ces deux calendriers, et quatre chiffres pour tous les autres calendriers pris en charge. Les calendriers qui comportent des années à un chiffre ou à deux chiffres, comme pour l’ère impériale japonaise, sont représentés différemment. Une année à un seul chiffre est représentée par un zéro non significatif, par exemple, « 03 ». Une année à deux chiffres est représentée par deux chiffres, par exemple, « 13 ». Aucun zéro non significatif supplémentaire n’est affiché. |
| yyyyy       | Se comporte de la même façon que « yyyy ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Le tableau suivant définit les types de format utilisés pour représenter un point ou une ère.



| Type de format | Signification                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, GG       | Chaîne de période/ère mise en forme comme spécifié par la \_ valeur Cal SERASTRING. Les images de format "g" et "GG" dans une chaîne de date sont ignorées s’il n’y a aucune chaîne d’ère ou de période associée. |



 

 

 




