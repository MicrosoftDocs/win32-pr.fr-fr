---
title: Type défini par l'utilisateur
description: Utilisez la syntaxe suivante pour déclarer un type défini par l’utilisateur.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379738"
---
# <a name="user-defined-type"></a><span data-ttu-id="f71d2-103">Type défini par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="f71d2-103">User-Defined Type</span></span>

<span data-ttu-id="f71d2-104">Utilisez la syntaxe suivante pour déclarer un type défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f71d2-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="f71d2-105">**\[ \] \[ index \] de nom de type const** typedef ;</span><span class="sxs-lookup"><span data-stu-id="f71d2-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f71d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f71d2-106">Parameters</span></span>



| <span data-ttu-id="f71d2-107">Élément</span><span class="sxs-lookup"><span data-stu-id="f71d2-107">Item</span></span>                                                                                         | <span data-ttu-id="f71d2-108">Description</span><span class="sxs-lookup"><span data-stu-id="f71d2-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71d2-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span><span class="sxs-lookup"><span data-stu-id="f71d2-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="f71d2-110">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f71d2-110">Optional.</span></span> <span data-ttu-id="f71d2-111">Ce mot clé marque explicitement le type en tant que constante.</span><span class="sxs-lookup"><span data-stu-id="f71d2-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="f71d2-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**</span><span class="sxs-lookup"><span data-stu-id="f71d2-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="f71d2-113">Identifie le type de données ; doit être l’un des types de données intrinsèques HLSL.</span><span class="sxs-lookup"><span data-stu-id="f71d2-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="f71d2-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="f71d2-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="f71d2-115">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="f71d2-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="f71d2-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Évaluer**</span><span class="sxs-lookup"><span data-stu-id="f71d2-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="f71d2-117">Taille de tableau facultative.</span><span class="sxs-lookup"><span data-stu-id="f71d2-117">Optional array size.</span></span> <span data-ttu-id="f71d2-118">Doit être un entier non signé compris entre 1 et 4 inclus.</span><span class="sxs-lookup"><span data-stu-id="f71d2-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="f71d2-119">En plus des types de données intrinsèques intégrés, le langage HLSL prend en charge les types définis par l’utilisateur ou personnalisés, qui suivent la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f71d2-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="f71d2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f71d2-120">Remarks</span></span>

<span data-ttu-id="f71d2-121">Les types définis par l’utilisateur ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="f71d2-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="f71d2-122">Pour plus de commodité, les types suivants sont définis automatiquement au niveau de la portée Super globale.</span><span class="sxs-lookup"><span data-stu-id="f71d2-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="f71d2-123">Le signe dièse ( \# ) représente un chiffre entier compris entre 1 et 4.</span><span class="sxs-lookup"><span data-stu-id="f71d2-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="f71d2-124">Pour la compatibilité avec les effets DirectX 8, les types suivants sont définis automatiquement au niveau de l’étendue Super globale :</span><span class="sxs-lookup"><span data-stu-id="f71d2-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="f71d2-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f71d2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f71d2-126">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f71d2-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





