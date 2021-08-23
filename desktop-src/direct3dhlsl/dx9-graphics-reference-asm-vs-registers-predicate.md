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
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119573"
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

 

 




