---
description: ID3DXInclude est une interface implémentée par l’utilisateur pour fournir des rappels pour les \# directives include pendant la compilation du nuanceur.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interface ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520351"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="f8c14-103">Interface ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="f8c14-103">ID3DXInclude interface</span></span>

<span data-ttu-id="f8c14-104">ID3DXInclude est une interface implémentée par l’utilisateur pour fournir des rappels pour les \# directives include pendant la compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f8c14-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="f8c14-105">Chacune des méthodes dans cette interface doit être implémentée par l’utilisateur qui sera ensuite utilisé comme rappels de l’application lorsque l’un des éléments suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="f8c14-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="f8c14-106">Un nuanceur HLSL qui contient un \# include est compilé en appelant l’une des \* \* \* fonctions D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="f8c14-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="f8c14-107">Un nuanceur \# d’assembly inclut est assemblé en appelant l’une des \* \* \* fonctions D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="f8c14-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="f8c14-108">Un effet qui contient un \# include est compilé par en appelant l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="f8c14-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="f8c14-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f8c14-109">Members</span></span>

<span data-ttu-id="f8c14-110">L’interface **ID3DXInclude** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f8c14-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8c14-111">**ID3DXInclude** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8c14-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="f8c14-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8c14-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f8c14-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8c14-113">Methods</span></span>

<span data-ttu-id="f8c14-114">L’interface **ID3DXInclude** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f8c14-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="f8c14-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="f8c14-115">Method</span></span>                               | <span data-ttu-id="f8c14-116">Description</span><span class="sxs-lookup"><span data-stu-id="f8c14-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8c14-117">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="f8c14-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="f8c14-118">Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f8c14-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="f8c14-119">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="f8c14-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="f8c14-120">Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f8c14-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8c14-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f8c14-121">Remarks</span></span>

<span data-ttu-id="f8c14-122">Un utilisateur crée une interface ID3DXInclude en implémentant une classe qui dérive de cette interface et en implémentant toutes les méthodes d’interface.</span><span class="sxs-lookup"><span data-stu-id="f8c14-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="f8c14-123">Le type LPD3DXINCLUDE est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="f8c14-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="f8c14-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8c14-124">Requirements</span></span>



| <span data-ttu-id="f8c14-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8c14-125">Requirement</span></span> | <span data-ttu-id="f8c14-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8c14-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c14-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8c14-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c14-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c14-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f8c14-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8c14-129">Library</span></span><br/> | <dl> <span data-ttu-id="f8c14-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8c14-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f8c14-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c14-132">Interfaces d’effet</span><span class="sxs-lookup"><span data-stu-id="f8c14-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
