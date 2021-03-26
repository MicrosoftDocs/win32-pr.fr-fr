---
title: Directives de préprocesseur (HLSL)
description: Les directives de préprocesseur, telles que \ define et \ ifdef, sont généralement utilisées pour rendre les programmes sources faciles à modifier et à compiler dans différents environnements d’exécution.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739229"
---
# <a name="preprocessor-directives-hlsl"></a>Directives de préprocesseur (HLSL)

Les directives de préprocesseur, telles que [ \# define](dx-graphics-hlsl-appendix-pre-define.md) et [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), sont généralement utilisées pour rendre les programmes sources faciles à modifier et à compiler dans différents environnements d’exécution. Les directives contenues dans le fichier source indiquent au préprocesseur d'exécuter des actions spécifiques. Par exemple, le préprocesseur peut remplacer des jetons dans le texte, insérer le contenu d'autres fichiers dans le fichier source ou supprimer la compilation d'une partie du fichier en supprimant des sections de texte. Les lignes de préprocesseur sont reconnues et exécutées avant l'expansion macro. Par conséquent, si une macro se développe en quelque chose qui ressemble à une commande de préprocesseur, cette commande n'est pas reconnue par le préprocesseur.

Les déclarations de préprocesseur utilisent le même jeu de caractères que les instructions de fichier source, sauf que les séquences d'échappement ne sont pas prises en charge. Le jeu de caractères utilisé dans les instructions de préprocesseur est identique au jeu de caractères d'exécution. Le préprocesseur reconnaît aussi les valeurs de caractères négatives.

Le préprocesseur HLSL reconnaît les directives suivantes :

-   [\#définition](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Erreurs](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#que](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#inclusion](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#spline](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

Le signe dièse ( \# ) doit être le premier caractère autre qu’un espace blanc sur la ligne contenant la directive ; les espaces blancs peuvent apparaître entre le signe dièse et la première lettre de la directive. Certaines directives incluent des arguments ou des valeurs. Tout texte qui suit une directive (sauf un argument ou une valeur qui fait partie de la directive) doit être précédé du délimiteur de commentaire sur une seule ligne (//) ou placé entre les délimiteurs de commentaires (/ \* \* /). Les lignes contenant des directives de préprocesseur peuvent être poursuivies en faisant immédiatement précéder le marqueur de fin de ligne d’une barre oblique inverse ( \) .

Les directives de préprocesseur peuvent apparaître n'importe où dans un fichier source, mais elles s'appliquent uniquement au reste du fichier source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annexe (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




