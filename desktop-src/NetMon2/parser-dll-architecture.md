---
description: L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architecture des DLL de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b2c3ead77d5172bc57fa3bc1c8b6001b9c690cd254dc436ac93f504ddb732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962862"
---
# <a name="parser-dll-architecture"></a>Architecture des DLL de l’analyseur

L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante. N’oubliez pas que certaines fonctionnalités nécessitent l’implémentation d’un seul point d’entrée. Toutefois, si votre DLL de l’analyseur prend en charge plusieurs protocoles, la fonctionnalité nécessite l’implémentation de plusieurs points d’entrée.

![fonctionnalités dll de l’analyseur](images/parserarchitecture1.png)



| Pour obtenir des informations sur                                                  | Consultez                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Comment implémenter les fonctions d’exportation de DLL de l’analyseur.                          | [Écriture d’un analyseur de protocole](writing-a-protocol-parser.md)             |
| Fonctions et structures spécifiques utilisées par les analyseurs : rubriques de référence. | [Structures et fonctions de l’analyseur](parser-functions-and-structures.md) |



 

 

 



