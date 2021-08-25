---
description: Les indicateurs D3DXSHADER sont utilisés pour analyser, compiler ou assembler des nuanceurs.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Indicateurs D3DXSHADER (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 031ae23301b78a9cced683551c9d7220aa66f7e0a48b504fe1a93721fd8d6a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849779"
---
# <a name="d3dxshader-flags"></a>Indicateurs D3DXSHADER

Les indicateurs **D3DXSHADER** sont utilisés pour analyser, compiler ou assembler des nuanceurs.

**Indicateurs de l’analyseur**

Les indicateurs de temps d’analyse sont utilisés uniquement par le système Effect (compilation avant effet) quand vous créez un compilateur Effect. Par exemple, vous pouvez créer un objet de compilateur avec **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**, puis utiliser cet objet de compilateur à plusieurs reprises avec différents indicateurs de compilateur pour générer du code spécialisé.



| Constante                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | À moins d’être explicitement spécifiés, les matrices sont compressées dans l’ordre des colonnes (chaque vecteur se trouve dans une seule colonne) lorsqu’elles sont transmises vers et depuis le nuanceur. Cette opération est généralement plus efficace, car elle permet d’effectuer une multiplication de matrice vectorielle à l’aide d’une série de produits point.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | Sauf spécification explicite, les matrices sont compressées dans l’ordre ligne-principal (chaque vecteur se trouve sur une seule ligne) lorsqu’il est passé au nuanceur ou à partir de celui-ci.<br/>                                                                                                                                        |



**Indicateurs du compilateur**

Le compilateur HLSL DirectX 10 est désormais le compilateur par défaut. Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .

Le tableau suivant détaille les indicateurs disponibles dans Direct3D 9 et Direct3D 10. La valeur de l’indicateur est l’option fxc équivalente.



| Constante/valeur                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ Évitez \_ \_ le contrôle de Flow**</dt> <dt>/GFA</dt> </dl>                                     | Il s’agit d’un indicateur permettant au compilateur d’éviter d’utiliser des instructions de contrôle de Flow.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ Déboguer**</dt> <dt>/Zi</dt> </dl>                                                                               | Insérez le nom de fichier de débogage, les numéros de ligne et les informations de type et de symbole lors de la compilation du nuanceur.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ ACTIVER la \_ \_ compatibilité descendante**</dt> <dt>/GEC</dt> </dl> | Compilez \_ \_ les nuanceurs PS 1 x en tant que PS \_ 2 \_ 0. Les effets qui spécifient \_ \_ les cibles PS 1 x vont plutôt être compilés en \_ cibles PS 2 \_ 0, car il s’agit de la version de nuanceur minimale prise en charge par la version du compilateur du nuanceur livré avec DirectX 10. Cet indicateur n’a aucun effet lorsqu’il est utilisé avec des cibles de compilation de niveau supérieur.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCER \_ le \_ logiciel PS \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Force le compilateur à effectuer une compilation en fonction de la cible de logiciel suivante la plus élevée disponible pour les nuanceurs de pixels. Cet indicateur active également les optimisations et le débogage sur.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCER \_ les \_ \_ NOOPT de logiciel vs**</dt> <dt>N/A</dt> </dl>                      | Force le compilateur à compiler en fonction de la cible de logiciel suivante la plus élevée disponible pour les nuanceurs de vertex. Cet indicateur active également les optimisations et le débogage sur.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ /GIS de la \_ strictité IEEE**</dt> <dt></dt> </dl>                                               | Désactiver les optimisations qui peuvent provoquer la différence entre la sortie d’un programme de nuanceur compilé et la sortie d’un programme compilé avec le compilateur de nuanceur DirectX 9 en raison des erreurs de faible précision dans les calculs à virgule flottante.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ AUCUN \_ préombrage**</dt> <dt>/op</dt> </dl>                                                         | Désactive les prénuanceurs. Le compilateur n’extraira pas les expressions statiques à des fins d’évaluation sur le processeur de l’ordinateur hôte. En outre, le compilateur ne gonflant aucune expression lors de la compilation de fonctions autonomes.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ /O0 de \_ niveau0 d’optimisation**</dt> <dt></dt> </dl>                                    | Niveau d’optimisation le plus bas. Peut générer du code plus lentement, mais le fera plus rapidement. Cela peut être utile dans un cycle de développement de nuanceur hautement itératif.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ OPTIMISATION du \_ niveau1**</dt> <dt>/O1</dt> </dl>                                    | Deuxième niveau d’optimisation le plus bas.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ /O2 \_ d’isolement2 d’optimisation**</dt> <dt></dt> </dl>                                    | Deuxième niveau d’optimisation le plus élevé.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ OPTIMISATION du \_ niveau3**</dt> <dt>/O3</dt> </dl>                                    | Niveau d’optimisation le plus élevé. Produit le meilleur code possible, mais peut prendre beaucoup plus de temps. Cela sera utile pour les versions finales d’une application où les performances sont le facteur le plus important.<br/> Direct3D 9-non<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/GPP</dt> </dl>                                             | Forcer tous les calculs du nuanceur résultant à se produire à la précision partielle. Cela peut entraîner une évaluation plus rapide des nuanceurs sur un matériel.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PRÉFÉRER \_ \_ le contrôle de Flow**</dt> <dt>/GFP</dt> </dl>                                  | Il s’agit d’un Conseil permettant au compilateur de préférer utiliser des instructions de contrôle de Flow.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/OD</dt> </dl>                                              | Indique au compilateur d’ignorer les étapes d’optimisation pendant la génération de code. Sauf si vous essayez d’isoler un problème dans votre code et que vous soupçonnez le compilateur, l’utilisation de cette option n’est pas recommandée.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/VD</dt> </dl>                                                    | Ne validez pas le code généré par rapport aux capacités et contraintes connues. Cette option est recommandée uniquement lors de la compilation de nuanceurs connus pour fonctionner (autrement dit, les nuanceurs qui ont été compilés avant sans cette option). Les nuanceurs sont toujours validés par le runtime avant d’être définis sur l’appareil.<br/> Direct3D 9-Oui<br/> Direct3D 10-Oui<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ UTILISER \_ Legacy \_ D3DX9 \_ 31 \_ dll**</dt> <dt>/LD</dt> </dl>                     | Activez l’utilisation du compilateur HLSL Direct3D 9 d’origine. OCT2006 \_ d3dx9 \_ 31 \_x86.cab ou OCT2006 \_ d3dx9 \_ 31 \_x64.cab doivent être inclus dans le cadre de la redistribution des applications. Cet indicateur est nécessaire pour compiler \_ \_ les nuanceurs PS 1 x sans utiliser l’indicateur de promotion sur PS \_ 2 \_ 0. La spécification de cet indicateur lors de l’obtention d’une interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) provoque des appels ultérieurs à [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) et [**CompileShader**](id3dxeffectcompiler--compileshader.md) via cet objet pour utiliser le compilateur hérité.<br/> Direct3D 9-Oui<br/> Direct3D 10-non<br/> |



**Indicateurs de l’assembleur**

Les indicateurs de l’assembleur sont utilisés par le système d’effet pour optimiser le code assembleur du nuanceur et de l’effet.



| Constante                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**Débogage D3DXSHADER \_**</dt> </dl>                                                          | Insérez le nom de fichier de débogage, les numéros de ligne et les informations de type et de symbole lors de la compilation du nuanceur.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ force \_ PS \_ Software \_ NOOPT**</dt> </dl> | Force le compilateur à effectuer une compilation en fonction de la cible de logiciel suivante la plus élevée disponible pour les nuanceurs de pixels. Cet indicateur active également les optimisations et le débogage sur.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ force \_ \_ NOOPT Software \_**</dt> </dl> | Force le compilateur à compiler en fonction de la cible de logiciel suivante la plus élevée disponible pour les nuanceurs de vertex. Cet indicateur active également les optimisations et le débogage sur.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | Ne validez pas le code généré par rapport aux capacités et contraintes connues. Cette option est recommandée uniquement lors de la compilation de nuanceurs connus pour fonctionner (autrement dit, les nuanceurs qui ont été compilés avant sans cette option). Les nuanceurs sont toujours validés par le runtime avant d’être définis sur l’appareil.<br/> |



## <a name="remarks"></a>Remarques

Le système Effect utilise les **indicateurs d’analyseur** lorsqu’il est appelé par les fonctions suivantes :

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

Le système Effect utilise des **indicateurs de compilateur** lorsqu’il est appelé par les fonctions suivantes :

-   [**D3DXCompileShader**](d3dxcompileshader.md) (ou [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) ou [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (ou [**CompileShader**](id3dxeffectcompiler--compileshader.md))

En outre, vous pouvez utiliser des **indicateurs de compilateur** lors de la création d’un effet en appelant [**D3DXCreateEffect**](d3dxcreateeffect.md) (ou [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)).

-   Si vous transmettez un fichier. FX non compilé, le système d’effet utilisera le paramètre d’entrée d’indicateur lors de la compilation.
-   Si vous passez un effet compilé, le système Effect ignore les indicateurs du compilateur, car ils ne sont pas nécessaires pour charger l’effet.

Le système Effect utilise les **indicateurs d’assembleur** lorsqu’il est appelé par les fonctions suivantes :

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

L’application d’indicateurs de **compilateur** ou d' **assembleurs** à l’API incorrecte provoquera l’échec de la validation du nuanceur. Vérifiez la valeur de retour du code d’erreur Direct3D de la fonction avec l’outil de recherche d’erreurs DirectX (DXErr.exe) pour faciliter le suivi de cette erreur. Vous pouvez obtenir DXErr.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
