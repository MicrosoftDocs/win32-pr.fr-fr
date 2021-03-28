---
title: Registre de prédicats (référence HLSL VS)
description: Ce registre de sortie du nuanceur de sommets contient une valeur booléenne par canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104030632"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Registre de prédicats (référence HLSL VS)

Ce registre de sortie du nuanceur de sommets contient une valeur booléenne par canal.

Un registre de prédicat est pris en charge par les versions suivantes.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de prédicat     |      |      |       | x    | x    | x     |



 

Voici les propriétés du Registre.



| Type de Registre | Count | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Prédicat (p)  | 1     | R/W (Lecture/écriture) | 1             | 1             | 4         | N/A     | None     | N            |



 

Le registre de prédicat peut être modifié avec [setp \_ COMP-vs](setp-comp---vs.md). Il n’y a aucune valeur par défaut pour ce registre, une application doit définir le registre avant de l’utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




