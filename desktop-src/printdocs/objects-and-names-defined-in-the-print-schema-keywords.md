---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objets et noms définis dans les mots clés du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211301"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Objets et noms définis dans les mots clés du schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’infrastructure du schéma d’impression définit un espace de noms qui comprend les éléments et les attributs XML définis dans les mots clés du schéma d’impression. Cela comprend des éléments tels que Feature, option et ScoredProperty ; les noms d’attributs tels que Name et Propagate ; valeurs et pour les attributs XML tels que contractions. En d’autres termes, chaque utilisation d’un nom défini dans les mots clés du schéma d’impression doit être explicitement qualifiée avec cet espace de noms, ou doit être implicitement associée à cet espace de noms par l’utilisation d’un attribut xmlns par défaut. Le document Mots clés du schéma d’impression définit les instances d’éléments publics qui peuvent apparaître dans n’importe quel contexte ou emplacement donné. Les instances d’élément doivent apparaître uniquement dans le contexte ou l’emplacement désigné dans l’infrastructure du schéma d’impression. Par exemple, le <fibres discontinues : option Name = "PSK : letter" > instance définie dans les mots clés du schéma d’impression doit apparaître dans l’instance <de fibres discontinues : Feature Name = "PSK : PageMediaSize" > (également définie dans les mots clés du schéma d’impression). Vous n’avez pas la liberté d’utiliser une instance d’option donnée en dehors de son contexte spécifié.

Les instances d’élément définies de manière privée peuvent apparaître n’importe où, à condition que le type d’élément apparaisse dans un contexte autorisé par l’infrastructure du schéma d’impression.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



