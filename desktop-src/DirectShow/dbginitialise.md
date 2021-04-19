---
description: La fonction DbgInitialise initialise la bibliothèque de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: DbgInitialise, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544013"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="fa8d5-104">DbgInitialise fonction)</span><span class="sxs-lookup"><span data-stu-id="fa8d5-104">DbgInitialise function</span></span>

<span data-ttu-id="fa8d5-105">La fonction **DbgInitialise** initialise la bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="fa8d5-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8d5-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="fa8d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa8d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa8d5-109">*hInst*</span><span class="sxs-lookup"><span data-stu-id="fa8d5-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="fa8d5-110">Handle de l’instance de module.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa8d5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa8d5-111">Return value</span></span>

<span data-ttu-id="fa8d5-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa8d5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fa8d5-113">Remarks</span></span>

<span data-ttu-id="fa8d5-114">Dans un fichier exécutable, appelez cette méthode avant d’utiliser les fonctionnalités de débogage DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="fa8d5-115">Avant la fermeture de l’exécutable, appelez la fonction [**DbgTerminate**](dbgterminate.md) pour nettoyer la bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="fa8d5-116">Dans une DLL qui établit un lien vers la bibliothèque de classes de base (Strmbase. lib), il n’est pas nécessaire d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="fa8d5-117">La fonction est appelée automatiquement lorsque la DLL est chargée.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8d5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa8d5-118">Requirements</span></span>



| <span data-ttu-id="fa8d5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa8d5-119">Requirement</span></span> | <span data-ttu-id="fa8d5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa8d5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8d5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa8d5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fa8d5-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa8d5-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa8d5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa8d5-123">Library</span></span><br/> | <dl> <span data-ttu-id="fa8d5-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fa8d5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa8d5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa8d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8d5-126">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="fa8d5-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




