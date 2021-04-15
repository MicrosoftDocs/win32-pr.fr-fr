---
title: Traitement des réservations
description: Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383211"
---
# <a name="processing-reservations"></a>Traitement des réservations

Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant. La racine de l’espace de noms URL pour HTTP appartient à l’administrateur système. Pour toutes les valeurs d’hôte et de port, les deux réservations suivantes sont toujours supposées à la racine de l’espace de noms **relativeUri** .



| Espace de noms réservé                 | Réservé pour              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Administrateur LocalSystem |
| https:// <host> :<port>/ | Administrateur LocalSystem |



 

Ces réservations implicites ne peuvent pas être supprimées. Toutefois, il est possible de déléguer des réservations racines explicites à d’autres utilisateurs. Les réservations comme ci-dessous créent des délégations de ce type :



| Espace de noms réservé        | Réservé pour |
|---------------------------|--------------|
| `https://+:80/`           | UtilisateurA, UtilisateurC reprennent |
| `https://adatum.com:443/` | Login        |



 

Si ces réservations déléguées sont supprimées par l’administrateur système, la propriété de l’espace de noms revient à la réservation implicite pour les valeurs d’hôte et de port correspondantes.

 

 




