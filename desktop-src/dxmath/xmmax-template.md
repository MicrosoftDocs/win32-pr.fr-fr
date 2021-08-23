---
description: Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus grande des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modèle XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362f486861400223024da5442c5103722bf35dcf8cba715da1397ad4b54c19b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117969"
---
# <a name="xmmax-template"></a>Modèle XMMax

Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus grande des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.

## <a name="syntax"></a>Syntaxe

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[dans \] spécifie le premier des deux objets.

</dd> <dt>

<span id="b"></span><span id="B"></span>*p*
</dt> <dd>

\[dans \] spécifie les deux des deux objets.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le plus grand des deux objets d’entrée.

## <a name="remarks"></a>Remarques

`XMMax` est un modèle et le type T est spécifié quand le modèle est instancié.

> [!Note]  
> Le `XMMax` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x. `XMMax` est disponible en tant que macro dans XNAMath 2. x.

 

> [!Note]  
> Dans l’idéal, utilisez std :: Max au lieu de `XMMax` . pour éviter les conflits avec les en-têtes de Windows avec std :: max, vous devez \# définir NOMINMAX avant d’inclure les en-têtes Windows.

 

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. pris en charge pour les applications de bureau Win32, les applications de Windows Store et les applications Windows Phone 8.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de modèle de bibliothèque DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 




