---
title: Registres-ds_5_0
description: Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de domaine version 5 \_ 0.
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311049"
---
# <a name="registers---ds_5_0"></a>Registres-DS \_ 5 \_ 0

Les registres d’entrée et de sortie suivants sont implémentés dans le nuanceur de domaine version 5 \_ 0.

## <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                              | Count                | R/W (Lecture/écriture) | Dimension                           | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                          | 4096 (r \# + x \# \[ n \] )   | R/W (Lecture/écriture) | 4                                   | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )                     | 4096 (r \# + x \# \[ n \] )   | R/W (Lecture/écriture) | 4                                   | Oui              | None     | Oui          |
| Points de contrôle d’entrée 32 bits ( \[ élément de vertex VCP \] \[ \] )     | 32 Voir la remarque 1 ci-dessous. | R   | 4 (composant) \* 32 (élément) \* 32 (vert) | Oui              | None     | Oui          |
| Constantes de correctif d’entrée 32 bits ( \[ vertex VPC \] )               | 32 Voir la remarque 2 ci-dessous. | R   | 4                                   | Oui              | None     | Oui          |
| emplacement d’entrée 32 bits dans le domaine (vDomain. XY, vDomain.xyz)) | 1                    | R   | 3                                   | Non               | N/A      | Oui          |
| PrimitiveID d’entrée UINT de 32 bits (vPrim)                      | 1                    | R   | 1                                   | Non               | N/A      | Oui          |
| Élément dans une ressource d’entrée (t \# )                         | 128                  | R   | 128                                 | Oui              | None     | Oui          |
| Échantillonneur (s \# )                                              | 16                   | R   | 1                                   | Oui              | None     | Oui          |
| Référence iConstantBuffer ( \# \[ index CB \] )                  | 15                   | R   | 4                                   | Oui              | None     | Oui          |
| iImmediate ConstantBuffer Reference ( \[ index ICB \] )         | 1                    | R   | 4                                   | Oui (contenu)    | Aucun     | Oui          |



 

**Remarque 1 :** Le nuanceur de domaine voit les sorties du nuanceur de coque dans 2 ensembles distincts de registres. Les registres VCP peuvent voir tous les points de contrôle de sortie du nuanceur de coque. Les registres VPC peuvent voir toutes les données de sortie de la constante de correction du nuanceur de coque.

**Remarque 2 :** Étant donné que le code pour les phases de mise à jour de la duplication de la coque ou de jointure constante TessFactors utilise des noms tels que SV \_ TessFactor, le nuanceur de domaine doit correspondre à ces déclarations sur l’entrée VPC équivalente s’il souhaite voir ces valeurs.

## <a name="output-registers"></a>Registres de sortie



| Type de Registre                           | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Élément de données de vertex de sortie 32 bits (o \# ) | 32    | W   | 4         | Oui              | None     | Oui          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




