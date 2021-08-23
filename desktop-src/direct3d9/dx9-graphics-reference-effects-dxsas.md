---
description: Les annotations et sémantiques standard (DXSAS) fournissent une méthode d’utilisation des nuanceurs de manière standard qui permet d’utiliser les nuanceurs avec les outils, les applications et les moteurs de jeux.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Informations de référence sur les annotations et sémantiques DirectX standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da1489f92fce16e4717d501a64ab862fb9292c271397aa4a77e00e74c2e7952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373632"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Informations de référence sur les annotations et sémantiques DirectX standard

Les annotations et sémantiques standard (DXSAS) fournissent une méthode d’utilisation des nuanceurs de manière standard qui permet d’utiliser les nuanceurs avec les outils, les applications et les moteurs de jeux. DXSAS définit un ensemble de sémantiques et d’annotations attachées aux valeurs de l’application hôte et aux paramètres Effects à des fins de partage d’effets. Pour que ces annotations et sémantiques soient utiles, elles doivent être implémentées à la fois dans l’application hôte et dans le fichier d’effet. Ce document décrit la norme DXSAS qui tire parti de la puissance de l’infrastructure d’effet DirectX pour permettre aux applications et aux outils hôtes de partager des effets DirectX (fichiers. FX) par programmation, ainsi que de concevoir l’interaction avec l’interface utilisateur.

## <a name="background-information"></a>Informations générales

Les annotations et sémantiques standard sont conçues pour lier les paramètres d’effet et de fichier X pour héberger des valeurs d’application. L’infrastructure d’effets D3DX (ou Effects) encapsule l’état de rendu. En encapsulant l’état de rendu (y compris l’état des vertex, des textures et du traitement des pixels), vous pouvez créer une bibliothèque d’effets couvrant un large éventail d’options de rendu. Cela peut inclure des options telles que le rendu sur différents types de matériel, ou le rendu avec une fusion simple ou à plusieurs passes. Pour plus d’informations sur l’infrastructure Effect, vous devez faire [référence à Effect](dx9-graphics-reference-effects.md). DXSAS s’appuie sur cette infrastructure pour offrir une expérience plus cohérente aux développeurs. Une fois que l’installation de rendu est encapsulée dans un effet, la norme DXSAS permet au développeur d’Effects d’exposer l’intention des paramètres d’effet par le biais d’annotations. Ces annotations peuvent ensuite être lues par n’importe quelle application hôte ou outil (pas seulement celle qui a été conçue pour utiliser l’effet) qui est conforme à la norme, comprendre comment utiliser l’effet de la manière qui a été conçue.

La normalisation de l’ensemble de la sémantique d’effet et des annotations qui hébergent les applications prennent en charge les auteurs d’effet d’autorisation pour créer des effets qui peuvent être utilisés dans plusieurs projets et promouvoir ainsi une plus grande communauté d’utilisateurs Effects. La norme DXSAS rend les fichiers lisibles par les développeurs, échangeables entre les outils et permet aux développeurs de tirer parti des outils tiers pour créer des effets pour leur pipeline.

Ce document décrit la norme DXSAS qui utilise des annotations pour exprimer l’intention des paramètres Effects, ainsi que la définition d’une collection de valeurs d’application hôte qui hébergent les applications qui sont convenues à être disponibles à un effet.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Effets de création avec des annotations et sémantiques standard

Comme vous pouvez le voir dans le diagramme suivant, la norme DXSAS nécessite des annotations dans un fichier d’effet, ainsi qu’une application hôte qui suit les instructions décrites ici pour utiliser le fichier.

![diagramme de la norme dxsas pour les applications hôtes et les fichiers Effects](images/sas-2.png)

L’application hôte doit implémenter la logique de l’interface utilisateur et l’environnement hôte. Pour implémenter des effets conformes à DXSAS, lisez les rubriques suivantes :

-   Le [paramètre global](global-parameter.md) définit des informations pertinentes pour l’effet, telles que la version ou l’auteur de l’effet.
-   La [liaison de données](data-binding.md) définit la collection de paramètres (ainsi que leur type et leur structure) qui peuvent être utilisés par un effet qui peut être défini par l’application hôte exposée aux effets.
-   Pour associer un contrôle d’interface utilisateur à un paramètre Effect, utilisez une [annotation d’interface](ui-annotation.md)utilisateur. Ces annotations sont notamment les suivantes : [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)et [SasUiStride](ui-annotation.md).
-   Pour initialiser un paramètre Effect avec les données contenues dans un fichier externe, utilisez une [annotation d’initialisation de paramètre](parameter-initialization-annotation.md).
-   Lorsque les données sont transférées entre l’application hôte et un effet (ou vice versa), le [Cast et la conversion](casting-and-conversion.md) se produisent lorsque les types ne correspondent pas exactement. Cette section spécifie la façon dont les données sont écrites en cas de différences entre les types source et cible. En outre, utilisez [ParameterValueModifiers](casting-and-conversion.md) pour modifier la façon dont l’application hôte doit interpréter les données lues à partir du paramètre Effect. Ces annotations sont notamment les suivantes : [SasNormalize](casting-and-conversion.md) et [SasUnits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Respect de la casse

Tous les identificateurs, la sémantique et les valeurs d’annotation ne respectent pas la casse. Les noms d’annotation (pas les valeurs) respectent la casse. Les noms d’annotations sont reconnus par le système D3DX Effects et, par conséquent, les noms d’annotations SAS le sont également.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence d’effet](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



