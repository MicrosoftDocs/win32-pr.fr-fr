---
description: Fonction de rappel pour UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342794"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="6d516-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="6d516-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="6d516-104">Fonction de rappel pour UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="6d516-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d516-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d516-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="6d516-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d516-106">Parameters</span></span>

<span data-ttu-id="6d516-107">\[\]fPercentDone : nombre à virgule flottante compris entre 0 et 1,0 qui représente le pourcentage de calculs effectués (entre 0 et 100 pour cent).</span><span class="sxs-lookup"><span data-stu-id="6d516-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="6d516-108">\[dans \] lpUserContext-pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="6d516-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d516-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d516-109">Return Value</span></span>

<span data-ttu-id="6d516-110">Cette fonction doit être implémentée pour retourner \_ OK pour continuer à exécuter le simulateur.</span><span class="sxs-lookup"><span data-stu-id="6d516-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="6d516-111">Toute autre valeur arrêtera le simulateur.</span><span class="sxs-lookup"><span data-stu-id="6d516-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d516-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d516-112">Remarks</span></span>

<span data-ttu-id="6d516-113">Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="6d516-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="6d516-114">Sinon, les dépassements de capacité de la pile peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="6d516-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="6d516-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d516-115">Requirement</span></span>                         | <span data-ttu-id="6d516-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d516-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="6d516-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d516-117">Header</span></span>                   | <span data-ttu-id="6d516-118">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="6d516-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="6d516-119">Bibliothèque d'importation</span><span class="sxs-lookup"><span data-stu-id="6d516-119">Import Library</span></span>           | <span data-ttu-id="6d516-120">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="6d516-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="6d516-121">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="6d516-121">Minimum Operating System</span></span> | <span data-ttu-id="6d516-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6d516-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="6d516-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d516-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d516-124">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="6d516-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
