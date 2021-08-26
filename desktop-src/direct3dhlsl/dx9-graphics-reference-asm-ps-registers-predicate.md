---
title: Registre de prédicats (référence PS HLSL)
description: Ce registre de sortie du nuanceur de pixels contient une valeur booléenne par canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cc8404c9a6be87951142ff3473b283a57f4814b729a8ad5a462f9069b20f3ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950029"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registre de prédicats (référence PS HLSL)

Ce registre de sortie du nuanceur de pixels contient une valeur booléenne par canal.

Un registre de prédicat est pris en charge par les versions suivantes :



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registre de prédicat    |      |      |      |      |      |       | x    | x    | x     |



 

Voici les propriétés du Registre.



| Type de Registre | Count | R/W (Lecture/écriture) | \# Ports de lecture | \# Lectures/inst | Dimension | RelAddr | Valeurs par défaut | DCL obligatoire |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Prédicat (p)  | 1     | R/W (Lecture/écriture) | 1             | 1             | 4         | N/A     | None     | N            |



 

Le registre de prédicat peut être modifié avec [setp \_ COMP-PS](setp-comp---ps.md). Il n’y a aucune valeur par défaut pour ce registre ; une application doit définir le registre avant de l’utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




