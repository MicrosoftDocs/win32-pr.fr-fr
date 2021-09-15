---
description: L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architecture des DLL de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311926"
---
# <a name="parser-dll-architecture"></a>Architecture des DLL de l’analyseur

L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante. N’oubliez pas que certaines fonctionnalités nécessitent l’implémentation d’un seul point d’entrée. Toutefois, si votre DLL de l’analyseur prend en charge plusieurs protocoles, la fonctionnalité nécessite l’implémentation de plusieurs points d’entrée.

![fonctionnalités dll de l’analyseur](images/parserarchitecture1.png)



| Pour obtenir des informations sur                                                  | Consultez                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Comment implémenter les fonctions d’exportation de DLL de l’analyseur.                          | [Écriture d’un analyseur de protocole](writing-a-protocol-parser.md)             |
| Fonctions et structures spécifiques utilisées par les analyseurs : rubriques de référence. | [Structures et fonctions de l’analyseur](parser-functions-and-structures.md) |



 

 

 



