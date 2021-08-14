---
title: Traitement des réservations
description: Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393761"
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

 

 




