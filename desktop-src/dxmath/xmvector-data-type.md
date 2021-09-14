---
description: Type portable utilisé pour représenter un vecteur de composants à virgule flottante ou entier 4 32 bits, chacun étant aligné de manière optimale et mappé à un registre de vecteur matériel.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Type de données XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292190"
---
# <a name="xmvector-data-type"></a>Type de données XMVECTOR

Type portable utilisé pour représenter un vecteur de composants à virgule flottante ou entier 4 32 bits, chacun étant aligné de manière optimale et mappé à un registre de vecteur matériel.

## <a name="remarks"></a>Notes

Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide `XMVECTOR` de lors de la programmation en C++, consultez [Extensions XMVECTOR](ovw-xmvector-extensions.md).

Dans la bibliothèque DirectXMath, pour prendre entièrement en charge la portabilité et l’optimisation, `XMVECTOR` est, par conception, un type opaque. L’implémentation réelle de dépend de la `XMVECTOR` plateforme.

En général, le code ne doit pas reposer sur les caractéristiques de toute implémentation spécifique à une plateforme donnée de `XMVECTOR` . Les implémentations spécifiques à la plateforme présentent les caractéristiques suivantes :

-   Ils ne sont pas portables.
-   Ils peuvent changer d’une version à l’autre.
-   L’utilisation inopportune des détails d’implémentation peut être non optimale.

Les développeurs doivent utiliser les fonctions d' [accesseur](ovw-xnamath-reference-functions-accessors.md), de [chargement](ovw-xnamath-reference-functions-load.md)et de [stockage](ovw-xnamath-reference-functions-storage.md) de la bibliothèque DirectXMath pour récupérer et définir les vecteurs, ainsi que les fonctions de Vector 4D de la [bibliothèque DirectXMath](ovw-xnamath-reference-functions-vector4.md) pour les manipuler.

Pour les projets qui requièrent des informations détaillées sur la façon d’implémenter `XMVECTOR` sur différentes plateformes, consultez [bibliothèques internes](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Alias de compilateur

Le fichier d’en-tête DirectXMath. h utilise des alias pour l' `XMVECTOR` objet, notamment **CXMVECTOR** et **FXMVECTOR**. L’en-tête utilise ces alias pour se conformer aux conventions d’appel optimales en ligne de différents compilateurs. Pour la plupart des projets qui utilisent DirectXMath, il suffit de traiter ces types comme un alias exact de `XMVECTOR` .

Par exemple :


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Pour les projets qui requièrent des informations détaillées sur la façon dont les différentes plateformes gèrent leurs conventions d’appel, consultez [bibliothèques internes](pg-xnamath-internals.md).

Pour XNAMATH 2. x, le `XMVECTOR` type de données contient des membres d’élément. x,. y,. z,. et. w, ce qui entraîne généralement une baisse des performances. L’utilisation du \_ \_ type strict VECTOR4 fournit un abonnement à la définition DirectXMath d’un type de données opaque.

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. pris en charge pour les applications de bureau Win32, les applications de Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de bibliothèque DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Type de données XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Type de données XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Type de données XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Type de données XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Type de données XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 




