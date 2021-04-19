---
description: Déclare un objet comme constante de sélection, afin d’éviter les rechargements redondants de cet objet s’il est utilisé (et déclaré) à plusieurs emplacements dans la bibliothèque DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529731"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="265dd-103">XMGLOBALCONST macro)</span><span class="sxs-lookup"><span data-stu-id="265dd-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="265dd-104">Déclare un objet comme constante de *sélection* , afin d’éviter les rechargements redondants de cet objet s’il est utilisé (et déclaré) à plusieurs emplacements dans la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="265dd-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="265dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="265dd-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="265dd-106">Notes</span><span class="sxs-lookup"><span data-stu-id="265dd-106">Remarks</span></span>

<span data-ttu-id="265dd-107">L’utilisation de XMGLOBALCONST permet de spécifier des constantes globales.</span><span class="sxs-lookup"><span data-stu-id="265dd-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="265dd-108">Cela permet de réduire la taille du segment de données d’une application, d’éviter la création et la destruction d’objets redondants, et de réduire les opérations de chargement et de stockage.</span><span class="sxs-lookup"><span data-stu-id="265dd-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="265dd-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="265dd-109">Requirements</span></span>

<span data-ttu-id="265dd-110">**En-tête :** Déclaré dans DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="265dd-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="265dd-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="265dd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265dd-112">Macros de la bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="265dd-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="265dd-113">Constantes globales dans la bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="265dd-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="265dd-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="265dd-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="265dd-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="265dd-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
