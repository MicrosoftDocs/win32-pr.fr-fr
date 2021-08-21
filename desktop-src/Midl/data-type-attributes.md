---
title: Attributs de type de données
description: Vous pouvez appliquer ces attributs aux types de données dans une instruction typedef pour définir plus précisément l’utilisation ou l’effet du type de données.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, attributs, type de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85142c13d9b478c449bf07955b85dd586b6312d891e17699861afb5bc2cc658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067369"
---
# <a name="data-type-attributes"></a>Attributs de type de données

Vous pouvez appliquer ces attributs aux types de données dans une instruction [**typedef**](typedef.md) pour définir plus précisément l’utilisation ou l’effet du type de données.



| Attribut                                 | Usage                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**handle de contexte \_**](context-handle.md) | Identifie un handle de liaison qui gère les informations d’État (contexte) sur un serveur particulier entre les appels de procédure distante d’un client particulier. Non valide pour les fonctions d’interface d' [**objet**](object.md) .                                                                                                         |
| [**traitée**](handle.md)                  | Spécifie un type de handle personnalisé propre à l’application.                                                                                                                                                                                                                                                                |
| [**MS \_ Union**](-ms-union.md)            | Contrôle l’alignement du rapport de non-remise des unions non encapsulées. Utilisez sur [**typedef**](typedef.md)s pour la compatibilité descendante avec les interfaces générées avec MIDL 1,0 ou 2,0.                                                                                                                                                            |
| [**canal**](pipe.md)                      | Autorise la transmission d’un flux ouvert de données typées à travers un appel de procédure distante. Un paramètre [**in**](in.md) pipe permet au serveur d’extraire le flux de données du client pendant un appel de procédure distante. Un paramètre de [**sortie**](-out.md) de canal permet au serveur d’envoyer à nouveau le flux de données au client. |
| [**transmettre \_ en tant que**](transmit-as.md)       | Spécifie la manière dont un type de données sera transmis sur un réseau, utilisé pour le marshaling personnalisé.                                                                                                                                                                                                                                  |
| [**\_enum v1**](v1-enum.md)               | Indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, au lieu de la valeur par défaut 16 bits.                                                                                                                                                                                                              |
| [**Marshal de câble \_**](wire-marshal.md)     | Semblable à [**transmit \_ As**](transmit-as.md) , mais vous implémentez les routines de dimensionnement, de marshaler, de démarshaler et de libération des données.                                                                                                                                                                                              |



 

 

 




