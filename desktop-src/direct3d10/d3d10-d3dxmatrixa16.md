---
description: 'D3DXMATRIXA16 structure (D3DX10Math. h) : matrice 4 x 4, alignée sur 16 octets, qui contient des méthodes et des surcharges d’opérateur.'
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: D3DXMATRIXA16, structure (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: e81071d44340ef7a4b874633e736e21016c697a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113187"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a><span data-ttu-id="46bb8-103">D3DXMATRIXA16, structure (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="46bb8-103">D3DXMATRIXA16 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="46bb8-104">Matrice 4 x 4 alignée sur 16 octets qui contient des méthodes et des surcharges d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="46bb8-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="46bb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46bb8-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="46bb8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="46bb8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="46bb8-107">**\_soudé**</span><span class="sxs-lookup"><span data-stu-id="46bb8-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="46bb8-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46bb8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="46bb8-109">Composant (i, j) de la matrice, où i est le numéro de ligne et j le numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="46bb8-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="46bb8-110">Par exemple, \_ 34 correspond à \[ un ₄ ₃ \] , le composant dans la troisième ligne et la quatrième colonne.</span><span class="sxs-lookup"><span data-stu-id="46bb8-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46bb8-111">Notes </span><span class="sxs-lookup"><span data-stu-id="46bb8-111">Remarks</span></span>

<span data-ttu-id="46bb8-112">Une matrice alignée sur 16 octets, quand elle est utilisée par les fonctions D3DX mathématiques, a été optimisée pour améliorer les performances sur les processeurs Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="46bb8-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="46bb8-113">Les matrices sont alignées indépendamment de l’endroit où elles sont créées : sur la pile du programme, dans le tas ou dans la portée globale.</span><span class="sxs-lookup"><span data-stu-id="46bb8-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="46bb8-114">L’alignement s’effectue à l’aide de \_ \_ declspec (align (16)), qui fonctionne avec Visual C++ .net et avec Visual C++ 6,0 uniquement lorsque le Pack de processeur est installé.</span><span class="sxs-lookup"><span data-stu-id="46bb8-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="46bb8-115">Malheureusement, il n’existe aucun moyen de détecter le Pack de processeur. par conséquent, l’alignement de l’octet est activé par défaut uniquement avec Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="46bb8-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="46bb8-116">Les vecteurs et les quaternions ne sont pas alignés sur les octets dans D3DX.</span><span class="sxs-lookup"><span data-stu-id="46bb8-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="46bb8-117">Lorsque vous utilisez des vecteurs et des quaternions avec des fonctions mathématiques D3DX, utilisez \_ declspec (align (16)) pour générer des vecteurs et des quaternions alignés sur un octet, car ils s’exécutent beaucoup mieux.</span><span class="sxs-lookup"><span data-stu-id="46bb8-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="46bb8-118">La définition de \_ declspec est indiquée ici.</span><span class="sxs-lookup"><span data-stu-id="46bb8-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="46bb8-119">D’autres compilateurs interprètent **D3DXMATRIXA16** comme [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="46bb8-119">Other compilers interpret **D3DXMATRIXA16** as [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span> <span data-ttu-id="46bb8-120">L’utilisation de cette structure sur un compilateur qui n’aligne pas réellement la matrice peut être problématique, car elle n’expose pas les bogues qui ignorent l’alignement.</span><span class="sxs-lookup"><span data-stu-id="46bb8-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="46bb8-121">Par exemple, si un objet **D3DXMATRIXA16** est à l’intérieur d’une structure ou d’une classe, une fonction [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) peut être effectuée avec un compactage étroit (en ignorant les limites de 16 octets).</span><span class="sxs-lookup"><span data-stu-id="46bb8-121">For example, if a **D3DXMATRIXA16** object is inside a structure or class, a [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="46bb8-122">Cela entraînerait des arrêts de build si le compilateur devait parfois ajouter l’alignement de matrice.</span><span class="sxs-lookup"><span data-stu-id="46bb8-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16-extensions"></a><span data-ttu-id="46bb8-123">Extensions D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="46bb8-123">D3DXMATRIXA16 Extensions</span></span>

<span data-ttu-id="46bb8-124">**D3DXMATRIXA16** a les extensions C++ suivantes.</span><span class="sxs-lookup"><span data-stu-id="46bb8-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="46bb8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46bb8-125">Requirements</span></span>



| <span data-ttu-id="46bb8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46bb8-126">Requirement</span></span> | <span data-ttu-id="46bb8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="46bb8-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46bb8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="46bb8-128">Header</span></span><br/> | <dl> <span data-ttu-id="46bb8-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="46bb8-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46bb8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46bb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46bb8-131">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="46bb8-131">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
