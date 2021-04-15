---
description: Définit des modèles binaires qui permettent des plans de découpage définis par l’utilisateur. Ces macros sont définies comme pratiques lors de la définition de valeurs pour l' \_ État de rendu D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: D3DCLIPPLANEn macro (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394087"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="9f486-104">D3DCLIPPLANEn macro)</span><span class="sxs-lookup"><span data-stu-id="9f486-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="9f486-105">Définit des modèles binaires qui permettent des plans de découpage définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f486-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="9f486-106">Ces macros sont définies comme pratiques lors de la définition de valeurs pour l' \_ État de rendu D3DRS CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="9f486-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f486-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f486-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="9f486-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f486-108">Parameters</span></span>

<span data-ttu-id="9f486-109">Cette macro n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9f486-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f486-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f486-110">Return value</span></span>

<span data-ttu-id="9f486-111">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f486-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f486-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9f486-112">Remarks</span></span>

<span data-ttu-id="9f486-113">Les plans de découpage définis par l’utilisateur sont activés lorsque la valeur définie dans l' \_ État de rendu D3DRS CLIPPLANEENABLE contient un ou plusieurs bits Set (autrement dit, n’est pas 0).</span><span class="sxs-lookup"><span data-stu-id="9f486-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="9f486-114">La valeur de l’État Render n’est pas importante. le système n’interprète pas la valeur comme un nombre.</span><span class="sxs-lookup"><span data-stu-id="9f486-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="9f486-115">Au lieu de cela, la valeur active le plan de découpage dont le bit correspondant est défini.</span><span class="sxs-lookup"><span data-stu-id="9f486-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="9f486-116">Le bit 0 contrôle l’état du premier plan de découpage (au niveau de l’index 0), le bit 1 le deuxième plan, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9f486-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="9f486-117">Les modèles de bits créés par ces macros peuvent être combinés à l’aide d’une opération OR logique pour activer simultanément plusieurs plans de découpage.</span><span class="sxs-lookup"><span data-stu-id="9f486-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="9f486-118">L’omission de l’une de ces macros dans la combinaison désactive efficacement le plan de découpage au niveau de cet index.</span><span class="sxs-lookup"><span data-stu-id="9f486-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f486-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f486-119">Requirements</span></span>



| <span data-ttu-id="9f486-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f486-120">Requirement</span></span> | <span data-ttu-id="9f486-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f486-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f486-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f486-122">Header</span></span><br/> | <dl> <span data-ttu-id="9f486-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f486-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f486-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f486-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f486-125">Macros</span><span class="sxs-lookup"><span data-stu-id="9f486-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




