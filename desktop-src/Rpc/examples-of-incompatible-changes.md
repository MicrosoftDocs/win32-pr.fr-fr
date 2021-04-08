---
title: Exemples de modifications incompatibles
description: 'En ce qui concerne les modifications incompatibles, la règle de pouce en cause est la suivante : toute modification peut être incompatible en amont, sauf si elle est très bien comprise.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029365"
---
# <a name="examples-of-incompatible-changes"></a>Exemples de modifications incompatibles

En ce qui concerne les modifications incompatibles, la règle de pouce est la suivante : toute modification peut être incompatible en amont, sauf si elle est très bien comprise. Cette règle requiert une connaissance des règles de NDR. Si vous ne connaissez pas le rapport de non-remise, n’apportez aucune modification. Les exemples de modifications qui entraînent généralement une violation d’accès dans l’application, ou une exception de données de stub incorrecte \_ \_ \_ déclenchée par le moteur de marshaling, sont les suivantes :

-   Ajout d’une nouvelle méthode au milieu des anciennes méthodes.
-   Ajout ou suppression de paramètres dans une méthode.
-   Modification d’un attribut, par exemple un attribut de pointeur : remplacement \[ \] de Ref par \[ unique \] ou \[ ptr, \] ou vice versa. Chaque type de pointeur a une représentation filaire différente.
-   Modification de la taille des données : de Short à long, de char à WCHAR \_ t (Unicode), en ajoutant un champ à une structure, en modifiant la taille d’un tableau de taille fixe.
-   Ajout de branches d’Union à une Union avec une clause default.

Il se peut que des modifications insidieux ou des incompatibilités involontaires entre un client et un serveur se produisent comme suit :

-   Modification d’un membre d’un type composé, tel qu’une structure ou un tableau. Par exemple, si un \_ ID client passe d’un entier à un GUID, une \_ structure d’enregistrement client avec le \_ champ ID client devient incompatible. Il peut être difficile de détecter s’il est monté en cascade sur plusieurs niveaux d’incorporation à un type de paramètre distant réel.
-   Modification d’un type importé. Le type peut provenir d’un autre composant qui n’est pas directement distant, par conséquent, la modification a été jugée compatible.
-   L’utilisation \# de ifdef dans un fichier IDL est une mauvaise idée pour les définitions de type ifdef dans un fichier IDL. il s’agit d’un incident qui se produit. Inévitablement, en raison de la génération ou d’autres problèmes, un client est compilé avec un ensemble différent de définitions que le serveur et il finit par être incompatible.

 

 




