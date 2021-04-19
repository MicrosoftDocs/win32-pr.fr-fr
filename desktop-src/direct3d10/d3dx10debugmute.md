---
description: Activez ou désactivez les messages de débogage.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: D3DX10DebugMute, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537273"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="b3fb5-103">D3DX10DebugMute fonction)</span><span class="sxs-lookup"><span data-stu-id="b3fb5-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="b3fb5-104">Activez ou désactivez les messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="b3fb5-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fb5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3fb5-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="b3fb5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3fb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3fb5-107">*Muet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3fb5-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fb5-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3fb5-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3fb5-109">Affectez la valeur **true** pour activer les messages de débogage ; Affectez la valeur **false** pour désactiver les messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="b3fb5-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3fb5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3fb5-110">Return value</span></span>

<span data-ttu-id="b3fb5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3fb5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3fb5-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b3fb5-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fb5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b3fb5-113">Remarks</span></span>

<span data-ttu-id="b3fb5-114">Utilisez cette fonction pour désactiver les messages d’erreur pour les API D3DX10 lors du débogage. l’utilisation de cette fonction doit être protégée par le \_ commutateur du compilateur de débogage d3d10.</span><span class="sxs-lookup"><span data-stu-id="b3fb5-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="b3fb5-115">L’État par défaut est **true** pour une version Debug.</span><span class="sxs-lookup"><span data-stu-id="b3fb5-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3fb5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3fb5-116">Requirements</span></span>



| <span data-ttu-id="b3fb5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3fb5-117">Requirement</span></span> | <span data-ttu-id="b3fb5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3fb5-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fb5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3fb5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b3fb5-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3fb5-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="b3fb5-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3fb5-121">Library</span></span><br/> | <dl> <span data-ttu-id="b3fb5-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3fb5-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3fb5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3fb5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fb5-124">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="b3fb5-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
