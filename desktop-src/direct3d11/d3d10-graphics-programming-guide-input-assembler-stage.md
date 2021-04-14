---
title: Étape de l’assembleur d’entrée
description: L’API Direct3D 10 et versions ultérieures sépare les zones fonctionnelles du pipeline en étapes ; la première étape du pipeline est l’étape de l’assembleur d’entrée (IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- étape assembleur d’entrée (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383360"
---
# <a name="input-assembler-stage"></a>Étape de l’assembleur d’entrée

L’API Direct3D 10 et versions ultérieures sépare les zones fonctionnelles du pipeline en étapes ; la première étape du pipeline est l’étape de l’assembleur d’entrée (IA).

L’objectif de l’étape assembleur d’entrée est de lire des données primitives (points, lignes et/ou triangles) à partir de mémoires tampons remplies par l’utilisateur et d’assembler les données dans des primitives qui seront utilisées par les autres étapes de pipeline. L’étape IA peut assembler des vertex dans plusieurs [types primitifs](d3d10-graphics-programming-guide-primitive-topologies.md) différents (tels que des listes de lignes, des bandes triangulaires ou des primitives avec contiguïté). Les nouveaux types primitifs (par exemple, une liste de lignes avec contiguïté ou une liste de triangles avec contiguïté) ont été ajoutés pour prendre en charge le nuanceur Geometry.

Les informations d’contiguïté sont visibles pour une application uniquement dans un nuanceur Geometry. Si un nuanceur Geometry a été appelé avec un triangle incluant une contiguïté, par exemple, les données d’entrée contiennent 3 sommets pour chaque triangle et 3 sommets pour les données d’contiguïté par triangle.

Lorsque l’étape d’assembleur d’entrée est demandée pour la sortie des données d’adjacence, les données d’entrée doivent inclure les données d’adjacence. Cela peut nécessiter la fourniture d’un vertex factice (formant un triangle dégenerate), ou peut-être en marquant l’un des attributs de vertex, que le vertex existe ou non. Elle doit également être détectée et gérée par un nuanceur Geometry, bien que l’élimination de la géométrie dégénérée se produise à l’étape de rastérisation.

Lors de l’assemblage de primitives, un objectif secondaire de l’IA est de joindre des [valeurs générées](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) par le système pour améliorer l’efficacité des nuanceurs. Les valeurs générées par le système sont des chaînes de texte qui sont également appelées sémantiques. Les trois étapes de nuanceur sont construites à partir d’un noyau de nuanceur commun et le noyau de nuanceur utilise des valeurs générées par le système (comme un ID primitif, un ID d’instance ou un ID de vertex) afin qu’une étape de nuanceur puisse réduire le traitement uniquement aux primitives, instances ou vertex qui n’ont pas encore été traités.

Comme indiqué dans le [diagramme de blocs de pipeline](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), une fois que l’étape IA lit les données à partir de la mémoire (assemble les données dans des primitives et attache les valeurs générées par le système), les données sont envoyées à l' [étape du nuanceur de sommets](/previous-versions//bb205146(v=vs.85)).


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Prise en main avec l’étape de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Quelques étapes sont nécessaires pour initialiser l’étape de l’assembleur d’entrée (IA). Par exemple, vous devez créer des ressources de mémoire tampon avec les données de vertex dont le pipeline a besoin, indiquer à l’étape IA où se trouvent les mémoires tampons et le type de données qu’elles contiennent, et spécifier le type de primitives à assembler à partir des données.<br/> |
| [Topologies de primitive](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 et versions ultérieures prennent en charge plusieurs types primitifs (ou topologies) représentés par le type énuméré de la [**\_ \_ topologie de la primitive D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Ces types définissent la façon dont les vertex sont interprétés et rendus par le pipeline.<br/>                                                          |
| [Utilisation de l’étape de Input-Assembler sans mémoires tampons](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | La création et la liaison de mémoires tampons ne sont pas nécessaires si vos nuanceurs ne nécessitent pas de tampons. Cette section contient un exemple de simples nuanceurs vertex et de pixels qui dessinent un triangle unique.<br/>                                                                                                                                  |
| [Utilisation des valeurs de System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Les valeurs générées par le système sont générées par l’étape IA (basée sur la [sémantique](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)d’entrée fournie par l’utilisateur) pour permettre une certaine efficacité dans les opérations de nuanceur. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

