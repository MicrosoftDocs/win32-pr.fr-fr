---
description: Fonction de rappel pour la simulation et la compression précalculées par luminance Transfer (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482088"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="af7ec-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="af7ec-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="af7ec-104">Fonction de rappel pour la simulation et la compression précalculées par luminance Transfer (PRT).</span><span class="sxs-lookup"><span data-stu-id="af7ec-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af7ec-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="af7ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af7ec-106">Parameters</span></span>

<span data-ttu-id="af7ec-107">fPercentDone : nombre à virgule flottante compris entre 0 et 1,0 qui représente le pourcentage de calculs effectués (entre 0 et 100 pour cent).</span><span class="sxs-lookup"><span data-stu-id="af7ec-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="af7ec-108">lpUserContext-pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="af7ec-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="af7ec-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af7ec-109">Return Value</span></span>

<span data-ttu-id="af7ec-110">Cette fonction doit être implémentée pour retourner \_ OK pour continuer à exécuter le simulateur.</span><span class="sxs-lookup"><span data-stu-id="af7ec-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="af7ec-111">Toute autre valeur arrêtera le simulateur.</span><span class="sxs-lookup"><span data-stu-id="af7ec-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="af7ec-112">Notes</span><span class="sxs-lookup"><span data-stu-id="af7ec-112">Remarks</span></span>

<span data-ttu-id="af7ec-113">Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="af7ec-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="af7ec-114">Sinon, les dépassements de capacité de la pile peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="af7ec-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="af7ec-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="af7ec-115">Header</span></span>                   | <span data-ttu-id="af7ec-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="af7ec-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="af7ec-117">Bibliothèque d'importation</span><span class="sxs-lookup"><span data-stu-id="af7ec-117">Import Library</span></span>           | <span data-ttu-id="af7ec-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="af7ec-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="af7ec-119">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="af7ec-119">Minimum Operating System</span></span> | <span data-ttu-id="af7ec-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="af7ec-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="af7ec-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af7ec-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af7ec-122">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="af7ec-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
