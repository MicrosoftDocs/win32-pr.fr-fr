---
description: Cette vue d’ensemble décrit les modifications requises pour migrer le code existant à l’aide de la bibliothèque Math XNA vers la bibliothèque DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migration de code à partir de la bibliothèque XNA Math
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126851607"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migration de code à partir de la bibliothèque XNA Math

Cette vue d’ensemble décrit les modifications requises pour migrer le code existant à l’aide de la bibliothèque Math XNA vers la bibliothèque DirectXMath.

## <a name="header-changes"></a>Modifications d’en-tête

La bibliothèque DirectXMath utilise un nouvel ensemble d’en-têtes.

Remplacez l' `xnamath.h` en-tête par `DirectXMath.h` et ajoutez `DirectXPackedVector.h` pour les types *empaquetés GPU* .

Les types englobants de l’exemple de collision du kit de développement logiciel (SDK) DirectX dans `xnacollision.h` font désormais partie de la bibliothèque DirectXMath dans `DirectXCollision.h` . Celles-ci ont été modifiées pour utiliser des classes C++ plutôt qu’une API de style C.

## <a name="constant-changes"></a>Modifications de constante

La \_ version XNAMATH (200, 201, 202, 203, 204, etc.) a été remplacée par la \_ version DIRECXTMATH (300, 301, 302, 303, etc.).

> [!NOTE]  
> DirectXMath 3,00 et 3,02 sont livrés avec des versions préliminaires du SDK Windows. DirectXMath 3,03 est dans la version finale du kit de développement logiciel (SDK) Windows 8.

## <a name="namespaces"></a>Espaces de noms

La bibliothèque DirectXMath utilise des espaces de noms C++ pour organiser les types. XNA Math a utilisé uniquement l’espace de noms global. Les types DirectXMath en commun avec XNA Math se trouvent dans l’espace de noms **DirectX** ou **DirectX ::P ackedvector** .

Dans les fichiers sources C++, une solution simple consiste à ajouter des `using` instructions.

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

Pour les en-têtes, il n’est pas recommandé d’ajouter des instructions using. Au lieu de cela, ajoutez des espaces de noms qualifiés complets.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Charges partielles

Pour les différentes fonctions qui chargent moins de 4 éléments d’un XMVECTOR, la bibliothèque mathématique XNA a laissé les éléments supplémentaires non définis. DirectXMath remplit toujours ces éléments supplémentaires avec 0.

## <a name="removal-of-xbox-360-specific-types"></a>Suppression de types spécifiques de Xbox 360

Les types, fonctions et constantes de bibliothèque mathématique XNA suivants ne sont pas disponibles dans DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g XMXorHenD3 \_ , g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g XMAddIco4 \_ , g \_ XMMulIco4

\_\_vector4i est déconseillé. Utilisez [**XMVECTORI32**](xmvectori32-data-type.md) ou [**XMVECTORU32**](xmvectoru32-data-type.md) à la place.

Les fonctions et types suivants sont déconseillés, car il s’agit uniquement de Xbox 360 : XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrinsèques ARM-néon

La déclaration d’une constante Vector avec ce code est compilée pour les mathématiques XNA pour SSE et non INTRINSÈQUEs, mais échoue pour DirectXMath à l’aide de ARM-néon.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

En général, nous ne recommandons pas cette méthode d’initialisation d’un [**XMVECTOR**](xmvector-data-type.md). Toutefois, si vous souhaitez une constante Vector, la classe [**XMVECTORF32**](xmvectorf32-data-type.md) prend en charge ce style d’initialisation et retourne le type **XMVECTOR** automatiquement afin que vous puissiez utiliser **XMVECTORF32** dans la plupart des contextes. Toutes les opérations d’écriture dans une classe **XMVECTORF32** nécessitent un référencement explicite du membre **XMVECTOR** . v.

## <a name="permute"></a>Permute

La bibliothèque mathématique XNA a la forme suivante :

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Pour DirectXMath, **XMVectorPermuteControl** a été éliminé et le XM \_ permute \_ 0x.. Les \_ \_ constantes de XM permute 1Z ont été redéfinies pour être des index simples de 0-7. Voici la nouvelle signature pour [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

Au lieu d’un mot de contrôle, cette fonction accepte directement les 4 index comme paramètres, ce qui la rend également analogue à la fonction [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) à l’aide du nouveau XM \_ SWIZZLE \_ X.. \_ \_ Les constantes XM SWIZZLE W sont définies comme des index 0-3 simples.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Pour les valeurs constantes, il existe un moyen bien plus efficace d’implémenter la permutation. Au lieu d’utiliser la forme de fonction de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), utilisez le formulaire de **modèle** :

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Formulaires de modèle

En général, l’utilisation d’un formulaire de modèle sur une forme de fonction des fonctions suivantes est bien plus efficace et permet à la bibliothèque d’effectuer des optimisations spécifiques à la plateforme par le biais de la spécialisation de modèle.

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a>Fonctions éliminées

| Fonction éliminée        | Remplacement                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
