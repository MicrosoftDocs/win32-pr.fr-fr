---
title: Mise en route (DirectXMath)
description: La bibliothèque DirectXMath implémente une interface optimale et portable pour les opérations algébriques arithmétiques et linéaires sur des vecteurs à virgule flottante simple précision (2D, 3D et 4D) ou des matrices (3 × 3 et 4 × 4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117499"
---
# <a name="getting-started-directxmath"></a>Mise en route (DirectXMath)

La bibliothèque DirectXMath implémente une interface optimale et portable pour les opérations algébriques arithmétiques et linéaires sur des vecteurs à virgule flottante simple précision (2D, 3D et 4D) ou des matrices (3 × 3 et 4 × 4). La bibliothèque dispose d’une prise en charge limitée pour les opérations de vecteur entier. Ces opérations sont largement utilisées pour le rendu et l’animation par les programmes graphiques. Il n’existe aucune prise en charge des vecteurs à double précision (y compris les longs, les shorts ou les octets) et les opérations de vecteur d’entiers limitées.

la bibliothèque est disponible sur une variété de plateformes de Windows. Étant donné que la bibliothèque fournit des fonctionnalités qui ne sont pas disponibles précédemment, cette version remplace les bibliothèques suivantes :

-   Bibliothèque mathématique Xbox fournie par l’en-tête Xboxmath. h
-   Bibliothèque D3DX 9 fournie par les dll D3DX 9
-   Bibliothèque mathématique D3DX 10 fournie par le biais des dll D3DX 10
-   Bibliothèque mathématique XNA fournie par l’en-tête xnamath. h dans le kit de développement logiciel (SDK) DirectX et Xbox 360 XDK

Ces sections décrivent les principes fondamentaux de la mise en route.

-   [Télécharger](#download)
-   [Configuration système requise pour l’exécution](#run-time-system-requirements)
-   [Vue d’ensemble de la conception](#design-overview)
-   [Convention de matrice](#matrix-convention)
-   [Utilisation de base](#basic-usage)
-   [Instructions d’utilisation de type](#type-usage-guidelines)
-   [Création de vecteurs](#creating-vectors)
    -   [VECTEURS DE CONSTANTE](#constant-vectors)
    -   [VECTEURS DE VARIABLES](#vectors-from-variables)
    -   [VECTEURS À PARTIR DE VECTEURS](#vectors-from-vectors)
    -   [VECTEURS DE LA MÉMOIRE](#vectors-from-memory)
-   [Extraction de composants à partir de vecteurs](#extracting-components-from-vectors)
-   [Rubriques connexes](#related-topics)

## <a name="download"></a>Télécharger

la bibliothèque DirectXMath est incluse dans le SDK Windows. vous pouvez également le télécharger à partir de [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Ce site contient également des exemples de projets associés.

## <a name="run-time-system-requirements"></a>Configuration système requise pour Run-Time

La bibliothèque DirectXMath utilise des instructions de processeur spécialisées pour les opérations vectorielles lorsqu’elles sont disponibles. Pour éviter qu’un programme ne génère des erreurs « exception d’instruction inconnue », vérifiez la prise en charge du processeur en appelant [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) avant d’utiliser la bibliothèque DirectXMath.

Voici les spécifications de base de la prise en charge de l’exécution de la bibliothèque DirectXMath :

-   la compilation par défaut sur une plateforme Windows (x86/x64) requiert la prise en charge des instructions SSE/SSE2.
-   la prise en charge par défaut sur une plateforme Windows RT nécessite une prise en charge des instructions ARM-néon.
-   La compilation avec [**\_ XM \_ aucune \_ intrinsèque \_**](ovw-xnamath-reference-directives.md) définie requiert uniquement la prise en charge de l’opération de calcul en virgule flottante standard.

> [!Note]  
> Quand vous appelez [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport), incluez <Windows. h> avant d’inclure <> DirectXMath. h. Il s’agit de la seule fonction de la bibliothèque qui requiert tout contenu de <Windows. h> vous n’êtes donc pas obligé d’inclure <> Windows. h dans chaque module qui utilise <DirectXMath. h>.

 

## <a name="design-overview"></a>Vue d’ensemble de la conception

La bibliothèque DirectXMath prend principalement en charge le langage de programmation C++. La bibliothèque est implémentée à l’aide de routines inline dans les fichiers d’en-tête, DirectXMath \* . inl, DirectXPackedVector. inl et DirectXCollision. inl. Cette implémentation utilise des intrinsèques du compilateur hautes performances.

La bibliothèque DirectXMath fournit les éléments suivants :

-   Implémentation utilisant des intrinsèques SSE/SSE2.
-   Implémentation sans intrinsèques.
-   Implémentation utilisant des intrinsèques ARM-néon.

Étant donné que la bibliothèque est distribuée à l’aide de fichiers d’en-tête, utilisez le code source pour personnaliser et optimiser pour votre propre application.

## <a name="matrix-convention"></a>Convention de matrice

DirectXMath utilise des matrices de lignes-principales, des vecteurs de ligne et la pré-multiplication. La main est déterminée par la version de fonction utilisée (RH et LH). sinon, la fonction fonctionne avec les coordonnées de la gauche ou de la main droite.

Pour référence, Direct3D a utilisé historiquement le système de coordonnées de gauche, les matrices de lignes principales, les vecteurs de ligne et la pré-multiplication. Direct3D moderne n’a pas d’exigence forte pour les coordonnées Left et Right-droitier, et en général, les nuanceurs HLSL utilisent par défaut des matrices de colonnes-principales. Pour plus d’informations, consultez [classement de matrices HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) .

## <a name="basic-usage"></a>Utilisation de base

Pour utiliser les fonctions de la bibliothèque DirectXMath, incluez les en-têtes DirectXMath. h, DirectXPackedVector. h, DirectXColors. h et/ou DirectXCollision. h. les en-têtes se trouvent dans le Kit de développement logiciel (sdk) Windows pour les applications Windows store.

## <a name="type-usage-guidelines"></a>Instructions d’utilisation de type

Les types [**XMVECTOR**](xmvector-data-type.md) et [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sont les chevaux de travail de la bibliothèque DirectXMath. Chaque opération consomme ou produit des données de ces types. Leur utilisation est essentielle à l’utilisation de la bibliothèque. Toutefois, étant donné que DirectXMath utilise les jeux d’instructions SIMD, ces types de données sont soumis à un certain nombre de restrictions. Il est essentiel que vous compreniez ces restrictions si vous souhaitez utiliser correctement les fonctions DirectXMath.

Vous devez considérer [**XMVECTOR**](xmvector-data-type.md) comme un proxy pour un registre matériel SIMD et [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) en tant que proxy pour un regroupement logique de quatre registres matériels SIMD. Ces types sont annotés pour indiquer qu’ils nécessitent un alignement sur 16 octets pour fonctionner correctement. Le compilateur les place automatiquement correctement sur la pile lorsqu’ils sont utilisés en tant que variable locale, ou les place dans le segment de données lorsqu’ils sont utilisés en tant que variable globale. Avec les conventions appropriées, elles peuvent également être transmises en toute sécurité en tant que paramètres d’une fonction (consultez [conventions d’appel](pg-xnamath-internals.md) pour plus d’informations).

Toutefois, les allocations à partir du tas sont plus compliquées. Par conséquent, vous devez faire attention lorsque vous utilisez [**XMVECTOR**](xmvector-data-type.md) ou [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) en tant que membre d’une classe ou d’une structure à allouer à partir du tas. sur Windows x64, toutes les allocations de tas sont alignées sur 16 octets, mais pour Windows x86, elles sont uniquement alignées sur 8 octets. Il existe des options pour allouer des structures à partir du tas avec alignement sur 16 octets (consultez [aligner correctement les allocations](pg-xnamath-optimizing.md)). Pour les programmes C++, vous pouvez utiliser les surcharges opérateur New/Delete/New \[ \] /Delete \[ \] (globalement ou propre à la classe) pour appliquer l’alignement optimal si vous le souhaitez.

> [!Note]  
> Comme alternative à l’application de l’alignement dans votre classe C++ directement par la surcharge de New/Delete, vous pouvez utiliser l' [idiome pImpl](https://en.wikipedia.org/wiki/Opaque_pointer). Si vous vous assurez que votre classe **IMPL** est alignée par le biais de [**\_ \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) en interne aligné, vous pouvez utiliser librement les types alignés dans l’implémentation interne. il s’agit d’une bonne option lorsque la classe « public » est une classe ref Windows Runtime ou prévue pour une utilisation avec le [**ptr std :: shared \_<>**](/cpp/standard-library/shared-ptr-class), ce qui peut autrement perturber l’alignement.

 

Toutefois, il est souvent plus facile et plus compact d’éviter d’utiliser [**XMVECTOR**](xmvector-data-type.md) ou [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) directement dans une classe ou une structure. Utilisez plutôt les [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3), [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4), [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3), [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4), etc., en tant que membres de votre structure. en outre, vous pouvez utiliser les fonctions de [chargement de vecteur](ovw-xnamath-reference-functions-load.md) et de [Stockage vectorielles](ovw-xnamath-reference-functions-storage.md) pour déplacer efficacement les données dans des variables locales **XMVECTOR** ou **XMMATRIX** , effectuer des calculs et stocker les résultats. Il existe également des fonctions de diffusion en continu ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream), etc.) qui fonctionnent efficacement directement sur les tableaux de ces types de données.

## <a name="creating-vectors"></a>Création de vecteurs

### <a name="constant-vectors"></a>VECTEURS DE CONSTANTE

De nombreuses opérations requièrent l’utilisation de constantes dans les calculs vectoriels, et il existe plusieurs façons de charger un [**XMVECTOR**](xmvector-data-type.md) avec les valeurs souhaitées.

-   Si vous chargez une constante scalaire dans tous les éléments d’un [**XMVECTOR**](xmvector-data-type.md), utilisez [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) ou [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Si vous utilisez une constante Vector avec des valeurs fixes différentes en tant que [**XMVECTOR**](xmvector-data-type.md), utilisez les structures [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** ou [**XMVECTORU8**](xmvectoru8-data-type.md) . Ils peuvent ensuite être référencés directement partout où vous transmettez une valeur **XMVECTOR** .
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > N’utilisez pas de listes d’initialiseurs directement avec [**XMVECTOR**](xmvector-data-type.md) (c’est-à-dire XMVECTOR v = {1.0 f, 2.0 f, 3.0 f, 4.0 f}). Ce code est inefficace et n’est pas portable sur toutes les plateformes prises en charge par DirectXMath.

     

-   DirectXMath comprend un certain nombre de constantes globales prédéfinies que vous pouvez utiliser dans votre code (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g XMHalfPi, \_ g \_ XMPi, etc.). Recherchez les valeurs **XMGLOBALCONSTANT** dans l’en-tête DirectXMath. h.
-   Il existe un ensemble de constantes vectorielles pour les couleurs RVB courantes (rouge, vert, bleu, jaune, etc.). Pour plus d’informations sur ces constantes vectorielles, consultez DirectXColors. h et l’espace de noms DirectX :: Colors.

### <a name="vectors-from-variables"></a>VECTEURS DE VARIABLES

-   Si vous créez un vecteur à partir d’une variable scalaire unique, consultez [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) et [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Si vous créez un vecteur à partir de quatre variables scalaires, consultez [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) et [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint).
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VECTEURS À PARTIR DE VECTEURS

-   Si vous créez un vecteur à partir d’un autre vecteur avec un composant spécifique défini sur une variable, vous pouvez envisager d’utiliser des [fonctions d’accesseur Vector](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Si vous créez un vecteur à partir d’un autre vecteur avec un seul composant répliqué, utilisez [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty), [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)et [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Si vous créez un vecteur à partir d’un autre vecteur ou d’une paire de vecteurs avec des composants réorganisés, consultez [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) et [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VECTEURS DE LA MÉMOIRE

-   Pour charger une valeur float unique à partir de la mémoire, consultez [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)et [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Les façons courantes de charger des tableaux de valeurs float sont les suivantes : [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)et [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   DirectXMath comprend un ensemble complet de types et de charges et de magasins associés pour gérer plusieurs structures de données et formats GPU courants. Consultez [Load Vector](ovw-xnamath-reference-functions-load.md) and [Vector Store](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Extraction de composants à partir de vecteurs

Le traitement SIMD est plus efficace lorsque les données sont chargées dans les registres SIMD et entièrement traitées avant l’extraction des résultats. La conversion entre les formes scalaire et vectorielle est inefficace. nous vous recommandons donc de le faire uniquement lorsque cela est nécessaire. Pour cette raison, les fonctions de la bibliothèque DirectXMath qui produisent une valeur scalaire sont retournées sous la forme d’un vecteur, où le résultat scalaire est répliqué dans le vecteur résultant (c’est-à-dire, [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length), etc.). Toutefois, lorsque vous avez besoin de valeurs scalaires, voici quelques options pour y accéder :

-   Si une réponse scalaire unique est calculée, l’utilisation des [fonctions d’accesseur de vecteur](ovw-xnamath-reference-functions-accessors.md) est appropriée :
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Si plusieurs composants du vecteur doivent être extraits, envisagez de stocker le vecteur dans une structure de mémoire et de le lire de nouveau. Par exemple :
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   La forme la plus efficace du traitement vectoriel consiste à utiliser la diffusion en continu de la mémoire vers la mémoire où les données d’entrée sont chargées à partir de la mémoire (à l’aide des [fonctions de chargement de vecteur](ovw-xnamath-reference-functions-load.md)), traitées entièrement sous forme de SIMD, puis écrites en mémoire (à l’aide des [fonctions Vector Store](ovw-xnamath-reference-functions-storage.md)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 