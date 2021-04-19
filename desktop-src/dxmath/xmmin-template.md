---
description: Compare deux instances de type de données numériques, ou deux instances d’un objet qui prend en charge une surcharge de <, et retourne la plus petite des deux instances. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modèle XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538574"
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

## <a name="remarks"></a>Notes

`XMMin` est un modèle et le type T est spécifié quand le modèle est instancié.

> [!Note]  
> Le `XMMin` modèle est nouveau pour DirectXMath et n’est pas disponible pour XNAMath 2. x. `XMMin` est disponible en tant que macro dans XNAMath 2. x.

 

> [!Note]  
> Dans l’idéal, utilisez std :: min au lieu de `XMMin` . Pour éviter les conflits avec les en-têtes Windows avec std :: min, vous devez \# définir NOMINMAX avant d’inclure les en-têtes Windows.

 

**Espace de noms**: utiliser DirectX

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8. Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.

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

 

 




