---
description: Les directives de compilateur ajustent les fonctionnalités utilisées par la bibliothèque DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Directives de compilateur de la bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127297106"
---
# <a name="directxmath-library-compiler-directives"></a>Directives de compilateur de la bibliothèque DirectXMath

Les directives de compilateur ajustent les fonctionnalités utilisées par la bibliothèque DirectXMath.



| Directive                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ aucune \_ intrinsèque\_        | Quand \_ XM \_ aucune \_ intrinsèque \_ n’est définie, les opérations DirectXMath sont implémentées sans utiliser d’intrinsèques spécifiques à la plateforme. Au lieu de cela, DirectXMath utilise uniquement des opérations à virgule flottante standard.<br/> Par défaut, \_ XM \_ aucune \_ intrinsèque \_ n’est définie.<br/> Cette directive remplace toutes les autres directives. Par conséquent, nous vous recommandons de rechercher \_ XM \_ non \_ intrinsèques \_ avant de déterminer l’état des intrinsèques de \_ XM ARM ou des intrinsèques \_ \_ \_ \_ \_ \_ SSE \_ \_ .<br/>                                                                              |
| \_XM \_ les \_ intrinsèques SSE\_       | Quand \_ XM \_ des \_ intrinsèques SSE \_ est défini, le code est compilé pour utiliser la prise en charge de SSE et SSE2 sur les plateformes qui prennent en charge ces jeux d’instructions.<br/> les versions Windows fournissant des intrinsèques sse prennent en charge les fonctions sse et SSE2.<br/> \_XM \_ \_ les intrinsèques SSE n' \_ ont aucun effet sur les systèmes qui ne prennent pas en charge SSE et SSE2.<br/> par défaut, \_ XM \_ SSE \_ intrinsèques \_ est défini lorsque les utilisateurs se compilent pour une plateforme Windows.<br/> DirectXMath utilise le compilateur standard définit ( \_ M \_ IX86/ \_ m \_ AMD64) pour déterminer Windows cibles x86 ou Windows x64.<br/> |
| \_XM \_ \_ fonctions d' \_ intrinsèques néon\_ | Cela indique que l’implémentation DirectXMath utilise des intrinsèques ARM-néon. par défaut, \_ XM \_ \_ \_ les intrinsèques de néon \_ est défini lorsque les utilisateurs se compilent pour une Windows sur une plateforme ARM/ARM64. DirectXMath utilise le compilateur standard define ( \_ m \_ ARM, \_ m \_ ARM64) pour déterminer cette cible binaire.<br/> La prise en charge des intrinsèques ARM-néon est une nouveauté de DirectXMath et n’est pas prise en charge par XNAMath 2. x.<br/>                                                                                                                                                                             |
| \_XM \_ SSE3 \_ intrinsèques\_      | Nouveauté de DirectXMath 3,10. <br/> Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath sont implémentées pour utiliser des intrinsèques SSE3, le cas échéant ; Sinon, elle utilise SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_XM \_ SSE4 \_ intrinsèques\_      | Nouveauté de DirectMath 3,09. <br/> Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath sont implémentées pour utiliser les intrinsèques SSE3 et SSE 4.1, le cas échéant ; Sinon, elle utilise SSE/SSE2. Lorsque vous spécifiez cette directive du compilateur, elle implique également des intrinsèques \_ XM \_ SSE3 \_ \_ et \_ XM les \_ \_ intrinsèques SSE \_ .<br/>                                                                                                                                                                                                                                |
| \_éléments \_ \_ intrinsèques AVX\_       | Nouveauté de DirectXMath 3,09. <br/> L’utilisation de/Arch : AVX active cette directive. <br/> Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath sont implémentées pour utiliser les intrinsèques SSE3, SSE 4.1 et AVX 128 bits, le cas échéant ; Sinon, DirectXMath utilise SSE/SSE2. Lorsque vous spécifiez cette directive du compilateur, elle implique également des intrinsèques \_ XM \_ SSE3 \_ , \_ XM \_ SSE4 \_ intrinsèques \_ et \_ XM des \_ \_ intrinsèques SSE \_ , et comprend un petit sous-ensemble d’instructions SSE3. <br/>                                                                    |
| XM \_ AVX2 \_ intrinsèques\_        | Nouveauté de DirectXMath 3,11. <br/> L’utilisation de/Arch : AVX2 active cette directive. Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath utilisent AVX2, F16C/CVT16, FMA3, AVX 128 bits, SSE 4.1 et SSE3 intrinsèques, le cas échéant. Lorsque vous utilisez \_ \_ \_ des intrinsèques XM AVX2 \_ , cela implique les intrinsèques \_ XM \_ F16C \_ \_ , \_ XM \_ FMA3 \_ intrinsèques \_ , \_ XM \_ AVX \_ intrinsèques \_ , \_ XM \_ SSE \_ intrinsèques \_ , \_ XM \_ SSE3 \_ intrinsèques \_ et \_ XM \_ SSE4 \_ intrinsic \_ .<br/>                                                                                       |
| \_XM \_ F16C \_ intrinsèques\_      | Nouveauté de DirectXMath 3,09. <br/> Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath sont implémentées pour utiliser les intrinsèques SSE3, SSE 4.1, AVX 128 bits et F16C/CVT16, le cas échéant ; Sinon, DirectXMath utilise SSE/SSE2. Lorsque vous utilisez \_ \_ des intrinsèques XM F16C, cela implique l’utilisation des intrinsèques \_ \_ \_ XM \_ \_ \_ , XM les intrinsèques \_ \_ SSE \_ \_ , \_ \_ \_ les intrinsèques SSE3 \_ et les \_ \_ \_ intrinsèques XM SSE4 \_ .<br/>                                                                                                                                                 |
| \_XM \_ FMA3 \_ intrinsèques\_      | Nouveauté de DirectXMath 3,11. <br/> Lorsque vous spécifiez cette directive du compilateur, les fonctions DirectXMath utilisent SSE3, SSE 4.1, AVX 128 bits et FMA3 intrinsèques, le cas échéant ; Sinon, DirectXMath utilise SSE/SSE2. Lorsque vous utilisez \_ \_ des intrinsèques XM FMA3, cela implique l’utilisation des intrinsèques \_ \_ \_ XM \_ \_ \_ , XM les intrinsèques \_ \_ SSE \_ \_ , \_ \_ \_ les intrinsèques SSE3 \_ et les \_ \_ \_ intrinsèques XM SSE4 \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | cela permet l’utilisation de la \_ \_ convention d’appel vectorcall pour les cibles Windows x86 ou Windows x64. La valeur par défaut est \_ XM \_ VECTORCALL \_ = 1 lorsque le compilateur prend en charge cette fonctionnalité. Vous pouvez le définir manuellement sur \_ XM \_ VECTORCALL \_ = 0 pour toujours le désactiver. <br/> \_\_vectorcall n’est pas pris en charge pour les Windows sur la plateforme ARM/ARM64 ou le C++ managé. <br/>                                                                                                                                                                                                                 |
| \_XM \_ SVML \_ intrinsèques\_     | Nouveauté de DirectXMath 3,16. <br/> Avec VS 2019 ou une version ultérieure, cela permet à la bibliothèque d’utiliser la &reg; bibliothèque Intel Short Vector Matrix pour x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
