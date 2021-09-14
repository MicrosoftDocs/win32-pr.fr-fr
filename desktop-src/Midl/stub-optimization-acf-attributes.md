---
title: Attributs ACF d’optimisation du stub
description: Ces attributs vous permettent d’optimiser la taille et la vitesse de votre code stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL, attributs, stub-optimisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093166"
---
# <a name="stub-optimization-acf-attributes"></a>Attributs ACF d’optimisation du stub

Ces attributs vous permettent d’optimiser la taille et la vitesse de votre code stub.



| Attribut                                    | Usage                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**code d’erreur**](code.md)[](nocode.md) | Utilisez les attributs [**code**](code.md) et [**nocode**](nocode.md) conjointement pour éviter de générer du code stub pour les fonctions inutilisées. Appliquez l’attribut **nocode** à l’en-tête d’interface et appliquez l’attribut **code** aux procédures que l’application cliente implémentera. Le code stub client est généré uniquement pour les procédures sélectionnées.                                                                |
| [**requêtes**](optimize.md)                 | Vous permet d’affiner le niveau d’optimisation effectué par le compilateur MIDL lors de la génération de code stub, en spécifiant que les données doivent être marshalées soit par la méthode en mode mixte, soit par la méthode interprétée. Vous pouvez appliquer l’attribut [**optimize**](optimize.md) à une interface ou à des fonctions sélectionnées dans l’interface. Dans les deux cas, son utilisation remplace les optimisations de ligne de commande et les valeurs par défaut préexistantes. |



 

 

 




