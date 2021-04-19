---
description: La \_ méthode obtenir le propriétaire récupère le propriétaire de la fenêtre active.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Méthode CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540288"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="1f3d4-103">CBaseControlWindow. obten, \_ méthode de propriétaire</span><span class="sxs-lookup"><span data-stu-id="1f3d4-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="1f3d4-104">La `get_Owner` méthode récupère le propriétaire de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f3d4-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="1f3d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f3d4-107">*Propriétaire*</span><span class="sxs-lookup"><span data-stu-id="1f3d4-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="1f3d4-108">Pointeur vers le propriétaire de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f3d4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f3d4-109">Return value</span></span>

<span data-ttu-id="1f3d4-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f3d4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f3d4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1f3d4-111">Remarks</span></span>

<span data-ttu-id="1f3d4-112">La fenêtre vidéo peut être lue dans un environnement de documents.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="1f3d4-113">Pour ce faire, la fenêtre doit être un enfant d’une autre fenêtre (afin qu’elle soit découpée et déplacée de manière appropriée).</span><span class="sxs-lookup"><span data-stu-id="1f3d4-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="1f3d4-114">Cette propriété permet de définir et de récupérer le propriétaire de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="1f3d4-115">Quand la fenêtre appartient à une autre fenêtre, elle appelle simplement la fonction Microsoft Win32 **SetParent,** .</span><span class="sxs-lookup"><span data-stu-id="1f3d4-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="1f3d4-116">Une application qui appelle cette fonction modifie les styles de fenêtre pour définir le \_ bit WS Child sur.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="1f3d4-117">Lorsque la fenêtre appartient à une autre fenêtre, elle transfère automatiquement certains ensembles de messages (en particulier, les messages de la souris et du clavier).</span><span class="sxs-lookup"><span data-stu-id="1f3d4-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="1f3d4-118">Cela permet à une application d’effectuer une modification simple à chaud et d’autres interactions.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="1f3d4-119">Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="1f3d4-120">Appelez la fonction membre [**CBaseControlWindow :: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="1f3d4-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f3d4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f3d4-121">Requirements</span></span>



| <span data-ttu-id="1f3d4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f3d4-122">Requirement</span></span> | <span data-ttu-id="1f3d4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f3d4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3d4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f3d4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1f3d4-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f3d4-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f3d4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f3d4-126">Library</span></span><br/> | <dl> <span data-ttu-id="1f3d4-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f3d4-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3d4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f3d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3d4-129">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="1f3d4-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




