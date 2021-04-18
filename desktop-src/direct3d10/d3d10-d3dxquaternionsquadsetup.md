---
description: Définit des points de contrôle pour l’interpolation sphérique Quadrangle.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: D3DXQuaternionSquadSetup, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523220"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>D3DXQuaternionSquadSetup, fonction (D3DX10Math. h)

Définit des points de contrôle pour l’interpolation sphérique Quadrangle.

## <a name="syntax"></a>Syntaxe


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAOut* \[ dans\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers sur.

</dd> <dt>

*pBOut* \[ dans\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers à propos de.

</dd> <dt>

*pCOut* \[ dans\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers COut.

</dd> <dt>

*pQ0* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers le point de contrôle d’entrée, Q0.

</dd> <dt>

*pQ1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers le point de contrôle d’entrée, Q1.

</dd> <dt>

*pQ2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers le point de contrôle d’entrée, Q2.

</dd> <dt>

*pQ3* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Pointeur vers le point de contrôle d’entrée, Q3.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucun.

## <a name="remarks"></a>Notes

Cette fonction prend quatre points de contrôle, qui sont fournis aux entrées pQ0, pQ1, pQ2 et pQ3. La fonction modifie ensuite ces valeurs pour trouver une courbe qui circule le long du chemin le plus rapide. Les valeurs de q0, Q2 et Q3 sont calculées comme indiqué ci-dessous.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Une fois les nouvelles valeurs Q calculées, les valeurs pour sur, à propos de et COut sont calculées comme suit :

Sur = T1 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q1) \* T2 \] \ + \ ln \[ exp (Q1) \* Q0 \] \) \ \] </sup>

À propos de = Q2 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (2e trimestre) \* Q3 \] \ + \ ln \[ exp (2e trimestre) \* Q1 \] \) \ \] </sup>

COut = Q2

> [!Note]  
> Ln est la méthode d’API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) et exp est la méthode d’API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

### <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser un ensemble de clés Quaternion (q0, T1, Q2, Q3) pour calculer les points Quadrangle internes (A, B, C). Cela permet de s’assurer que les tangentes sont continues sur les segments adjacents.


```
      A     B
Q0    Q1    Q2    Q3
```



L’exemple de code suivant montre comment vous pouvez interpoler entre Q1 et Q2.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C est +/-Q2 en fonction du résultat de la fonction.
> -   Qt est le résultat de la fonction.
>
> Le résultat est une rotation de 45 degrés autour de l’axe z pour Time = 0,5.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
