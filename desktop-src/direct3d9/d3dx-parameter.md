---
description: Ces indicateurs fournissent des informations supplémentaires sur les paramètres d’effet.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 5314ae0a13f6b9f4e246cc61c33ce626f217a4d654de2f582d18027c952bd2a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607809"
---
# <a name="d3dx_parameter"></a>\_Paramètre D3DX

Ces indicateurs fournissent des informations supplémentaires sur les paramètres d’effet.

Les constantes de paramètre d’effet sont utilisées par [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).



| Constante                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**\_Annotation de paramètre D3DX \_**</dt> </dl> | Ce paramètre est marqué comme une annotation. Consultez [Ajouter des informations pour appliquer des paramètres avec des annotations](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**D3DX \_ , \_ littéral de paramètre**</dt> </dl>          | Ce paramètre est marqué en tant que valeur littérale. Les paramètres Literal ne peuvent pas être modifiés après la compilation, ce qui permet au compilateur d’optimiser leur utilisation. Les paramètres partagés ne peuvent pas être marqués comme un littéral. Consultez [utilisations et littéraux (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**\_Paramètre D3DX \_ partagé**</dt> </dl>             | La valeur d’un paramètre est partagée par tous les effets dans le même espace de noms. La modification de la valeur dans un effet entraîne sa modification dans tous les effets partagés. Consultez [partage de paramètres](cloning-and-sharing.md). **D3DX \_ Le paramètre \_ Shared** ne peut pas être combiné avec un **\_ \_ littéral de paramètre D3DX** ou une **\_ \_ annotation de paramètre D3DX**.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’effet](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




