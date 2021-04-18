---
description: La fonction GetDialogSize récupère la taille d’une boîte de dialogue de ressource.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: GetDialogSize, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533160"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="9413b-103">GetDialogSize fonction)</span><span class="sxs-lookup"><span data-stu-id="9413b-103">GetDialogSize function</span></span>

<span data-ttu-id="9413b-104">La fonction **GetDialogSize** récupère la taille d’une boîte de dialogue de ressource.</span><span class="sxs-lookup"><span data-stu-id="9413b-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="9413b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9413b-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="9413b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9413b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9413b-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="9413b-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="9413b-108">Identificateur de ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9413b-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9413b-109">*pDlgProc*</span><span class="sxs-lookup"><span data-stu-id="9413b-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="9413b-110">Pointeur désignant la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9413b-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="9413b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9413b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9413b-112">Valeur transmise dans le \_ message WM INITDIALOG envoyé à la boîte de dialogue temporaire juste après sa création.</span><span class="sxs-lookup"><span data-stu-id="9413b-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="9413b-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="9413b-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="9413b-114">Pointeur vers une structure de **taille** qui reçoit les dimensions de la boîte de dialogue, en pixels d’écran.</span><span class="sxs-lookup"><span data-stu-id="9413b-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9413b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9413b-115">Return value</span></span>

<span data-ttu-id="9413b-116">Retourne la **valeur true** si la ressource de boîte de dialogue a été trouvée, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9413b-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9413b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9413b-117">Remarks</span></span>

<span data-ttu-id="9413b-118">Les pages de propriétés peuvent utiliser cette fonction pour retourner la taille d’affichage réelle dont elles ont besoin.</span><span class="sxs-lookup"><span data-stu-id="9413b-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="9413b-119">La plupart des pages de propriétés sont des boîtes de dialogue et, par conséquent, ont des modèles de boîte de dialogue stockés dans des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="9413b-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="9413b-120">Les modèles utilisent des unités de boîte de dialogue qui ne correspondent pas directement aux pixels de l’écran.</span><span class="sxs-lookup"><span data-stu-id="9413b-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="9413b-121">Toutefois, la fonction [**GetPageInfo**](cbasepropertypage-getpageinfo.md) d’une page de propriétés doit retourner la taille réelle de l’affichage en pixels.</span><span class="sxs-lookup"><span data-stu-id="9413b-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="9413b-122">La page de propriétés peut appeler `GetDialogSize` pour calculer la taille de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9413b-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="9413b-123">Cette fonction crée une instance temporaire de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9413b-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="9413b-124">Pour éviter que la boîte de dialogue ne s’affiche à l’écran, le modèle de boîte de dialogue dans le fichier de ressources ne doit pas avoir de \_ propriété WS visible.</span><span class="sxs-lookup"><span data-stu-id="9413b-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9413b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9413b-125">Requirements</span></span>



| <span data-ttu-id="9413b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9413b-126">Requirement</span></span> | <span data-ttu-id="9413b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9413b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9413b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9413b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9413b-129"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9413b-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9413b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9413b-130">Library</span></span><br/> | <dl> <span data-ttu-id="9413b-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9413b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9413b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9413b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9413b-133">Fonctions d’assistance de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="9413b-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




