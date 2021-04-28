---
description: 'D3DXMATRIXA16 structure (D3dx9math. h) : matrice 4 x 4, alignée sur 16 octets, qui contient des méthodes et des surcharges d’opérateur.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: D3DXMATRIXA16, structure (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094207"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>D3DXMATRIXA16, structure (D3dx9math. h)

Matrice 4 x 4 alignée sur 16 octets qui contient des méthodes et des surcharges d’opérateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_soudé**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Composant (i, j) de la matrice, où i est le numéro de ligne et j le numéro de colonne. Par exemple, \_ 34 correspond à \[ un ₄ ₃ \] , le composant dans la troisième ligne et la quatrième colonne.

</dd> </dl>

## <a name="remarks"></a>Notes 

Une matrice alignée sur 16 octets, quand elle est utilisée par les fonctions D3DX mathématiques, a été optimisée pour améliorer les performances sur les processeurs Intel Pentium 4. Les matrices sont alignées indépendamment de l’endroit où elles sont créées : sur la pile du programme, dans le tas ou dans la portée globale. L’alignement s’effectue à l’aide de \_ \_ declspec (align (16)), qui fonctionne avec Visual C++ .net et avec Visual C++ 6,0 uniquement lorsque le Pack de processeur est installé. Malheureusement, il n’existe aucun moyen de détecter le Pack de processeur. par conséquent, l’alignement de l’octet est activé par défaut uniquement avec Visual C++ .NET.

Les vecteurs et les quaternions ne sont pas alignés sur les octets dans D3DX. Lorsque vous utilisez des vecteurs et des quaternions avec des fonctions mathématiques D3DX, utilisez \_ declspec (align (16)) pour générer des vecteurs et des quaternions alignés sur un octet, car ils s’exécutent beaucoup mieux. La définition de \_ declspec est indiquée ici.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



D’autres compilateurs interprètent D3DXMATRIXA16 comme D3DXMATRIX. L’utilisation de cette structure sur un compilateur qui n’aligne pas réellement la matrice peut être problématique, car elle n’expose pas les bogues qui ignorent l’alignement. Par exemple, si un objet D3DXMATRIXA16 est à l’intérieur d’une structure ou d’une classe, une fonction [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) peut être effectuée avec un compactage étroit (en ignorant les limites de 16 octets). Cela entraînerait des arrêts de build si le compilateur devait parfois ajouter l’alignement de matrice.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

**D3DXMATRIXA16** a les extensions C++ suivantes.


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
