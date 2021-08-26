---
title: GetSamplePosition (objet texture HLSL DirectX)
description: Obtient la position de l’échantillon spécifié.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95be6d9b6c4cbf70aed059399af0892a3c75f0a3462b6ef2b0732e8180f4e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068109"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (objet texture HLSL DirectX)

Obtient la position de l’échantillon spécifié.

RET Object. GetSamplePosition (int s);



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                           | Description                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*<br/> | Type d' [objet de texture](dx-graphics-hlsl-to-type.md) Texture2DMS ou Texture2DMSArray.<br/> |
| <span id="s"></span><span id="S"></span>*x*<br/>                                         | \[dans \] l’exemple d’index de base zéro.<br/>                                                      |



 

## <a name="return-value"></a>Valeur renvoyée

Retourne la position d’échantillon (x, y), un vecteur à virgule flottante à deux composants.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="remarks"></a>Remarques

Un nuanceur de pixels peut être évalué à la fréquence d’échantillonnage (exécuter un nuanceur de pixels une fois par échantillon) ou à fréquence en pixels (exécuter un nuanceur de pixels une fois par pixel). Attacher la \_ sémantique SV SampleIndex à une entrée de nuanceur de pixels pour appeler un nuanceur de pixels à la fréquence d’échantillonnage, la valeur d’entrée est ensuite utilisée comme exemple d’index lors de l’échantillonnage de la cible de rendu.

Vous pouvez interpoler une entrée de nuanceur de pixels de plusieurs façons. Pour interpoler à :

-   Un centre de pixels, n’utilisez aucune sémantique.
-   Un exemple, utilisez la \_ sémantique SV SampleIndex.
-   Un emplacement de centre de gravité, utilisez le modificateur de centre de [ \_ gravité](dx-graphics-hlsl-struct.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





