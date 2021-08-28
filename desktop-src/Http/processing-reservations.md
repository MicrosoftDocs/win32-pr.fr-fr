---
title: Traitement des réservations
description: Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aefbc72d5ea373765db674c3d4815f2a4cfa0a6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882813"
---
# <a name="processing-reservations"></a>Traitement des réservations

Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant. La racine de l’espace de noms URL pour HTTP appartient à l’administrateur système. Pour toutes les valeurs d’hôte et de port, les deux réservations suivantes sont toujours supposées à la racine de l’espace de noms **relativeUri** .



| Espace de noms réservé                 | Réservé pour              |
|------------------------------------|---------------------------|
| &lt;hôte https:// &gt; : &lt; port&gt;/  | Administrateur LocalSystem |
| &lt;hôte https:// &gt; : &lt; port&gt;/ | Administrateur LocalSystem |



 

Ces réservations implicites ne peuvent pas être supprimées. Toutefois, il est possible de déléguer des réservations racines explicites à d’autres utilisateurs. Les réservations comme ci-dessous créent des délégations de ce type :



| Espace de noms réservé        | Réservé pour |
|---------------------------|--------------|
| `https://+:80/`           | UtilisateurA, UtilisateurC reprennent |
| `https://adatum.com:443/` | Login        |



 

Si ces réservations déléguées sont supprimées par l’administrateur système, la propriété de l’espace de noms revient à la réservation implicite pour les valeurs d’hôte et de port correspondantes.

 

 




