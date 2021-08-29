---
title: Attributs de performance
description: Utilisez les attributs suivants dans un fichier IDL pour réduire la taille du code stub ou pour améliorer les performances.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL, attributs, performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f784bc534fd1dd7f160eaccb87a2853d491237db915245d4f36823e1ceb559ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869459"
---
# <a name="performance-attributes"></a>Attributs de performance

Utilisez les attributs suivants dans un fichier IDL pour réduire la taille du code stub ou pour améliorer les performances.



| Attribut                             | Usage                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tenir**](ignore.md)              | Désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur ne doit pas être transmis.                        |
| [**local**](local.md)                | Désigne une fonction qui est locale à l’application pour laquelle MIDL n’a pas besoin de générer de code stub.                                           |
| [**Marshal de câble \_**](wire-marshal.md) | Définit un type de données comme type plus simple pour la transmission sur un réseau et vous permet d’implémenter des routines de marshaling et de démarshaling pour le type. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs ACF de gestion de la mémoire](memory-management-acf-attributes.md)
</dt> <dt>

[Attributs ACF d’optimisation du stub](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




