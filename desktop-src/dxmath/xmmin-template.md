---
description: Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus petite des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modèle XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499854"
---
# <a name="xmmin-template"></a>Modèle XMMin

Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus petite des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.

## <a name="syntax"></a>Syntaxe

``` syntax
template<class T> T XMMin(
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

Retourne le plus petit des deux objets d’entrée.

## <a name="remarks"></a>Remarques

`XMMin` est un modèle et le type T est spécifié quand le modèle est instancié.

> [!Note]  
> Le `XMMin` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x. `XMMin` est disponible en tant que macro dans XNAMath 2. x.

 

> [!Note]  
> Dans l’idéal, utilisez std :: min au lieu de `XMMin` . pour éviter les conflits avec les en-têtes de Windows avec std :: min, vous devez \# définir NOMINMAX avant d’inclure les en-têtes Windows.

 

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

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




