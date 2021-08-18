---
description: Vos applications doivent utiliser le caractère de séparation de ligne (0x2028) et le caractère de séparation de paragraphe (0x2029) pour diviser le texte brut. Une ligne est créée après chaque séparateur de lignes. Un paragraphe est créé après chaque séparateur de paragraphes.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Utilisation de séparateurs de ligne et de paragraphe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d7cae4dc7bd720ca94e9780bcb83588650b3df578cd0216e2424c1b28d5af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764629"
---
# <a name="using-line-and-paragraph-separators"></a>Utilisation de séparateurs de ligne et de paragraphe

Vos applications doivent utiliser le caractère de séparation de ligne (0x2028) et le caractère de séparation de paragraphe (0x2029) pour diviser le texte brut. Une ligne est créée après chaque séparateur de lignes. Un paragraphe est créé après chaque séparateur de paragraphes.

Il n’est pas nécessaire de commencer la première ligne ou le premier paragraphe dans un fichier contenant ces caractères ou de mettre fin à la dernière ligne ou au dernier paragraphe. Cela indique qu’il y a une ligne ou un paragraphe vide à cet emplacement.

L’application peut utiliser le séparateur de ligne pour indiquer une fin de ligne inconditionnelle. Toutefois, les séparateurs de lignes ne correspondent pas aux caractères distincts de retour chariot et de saut de ligne, ni à une combinaison de ces caractères. Les séparateurs de lignes doivent être traités séparément des caractères de saut de ligne et de retour chariot.

L’application peut insérer un séparateur de paragraphe entre des paragraphes de texte. L’utilisation de ce séparateur vous permet de créer des fichiers de texte brut qui peuvent être mis en forme avec des largeurs de ligne distinctes sur différents systèmes d’exploitation. Le système cible peut ignorer les séparateurs de lignes et interrompre les paragraphes uniquement au niveau des séparateurs de paragraphes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



