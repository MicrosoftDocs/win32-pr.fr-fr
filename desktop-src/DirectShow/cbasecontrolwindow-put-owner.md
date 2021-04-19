---
description: La \_ méthode put owner définit la fenêtre parente de la fenêtre vidéo ; la fenêtre parente transfère ensuite certains messages à la fenêtre vidéo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Méthode CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545629"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="8faca-103">Méthode de propriétaire CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="8faca-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="8faca-104">La `put_Owner` méthode définit la fenêtre parente de la fenêtre vidéo ; la fenêtre parente transfère ensuite certains messages à la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="8faca-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8faca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8faca-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="8faca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8faca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8faca-107">*Propriétaire*</span><span class="sxs-lookup"><span data-stu-id="8faca-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="8faca-108">Handle vers la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="8faca-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8faca-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8faca-109">Return value</span></span>

<span data-ttu-id="8faca-110">Retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="8faca-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8faca-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8faca-111">Remarks</span></span>

<span data-ttu-id="8faca-112">En interne, cette méthode appelle la fonction Microsoft Win32 **SetParent,** pour définir le nouveau propriétaire et définit le style de la fenêtre parente sur WS \_ Child.</span><span class="sxs-lookup"><span data-stu-id="8faca-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="8faca-113">La fenêtre parente transmet ensuite certains ensembles de messages (en particulier, les messages de souris et de clavier) à la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="8faca-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="8faca-114">Une fois que vous avez défini le propriétaire de la fenêtre vidéo, vous devez définir le propriétaire sur la **valeur null** et le style de fenêtre du propriétaire sur WS \_ OVERLAPPED et WS \_ CLIPCHILDREN avant de libérer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8faca-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="8faca-115">Lorsque vous affectez la valeur **null** au propriétaire, cette méthode désactive le bit WS Child de la fenêtre parente \_ .</span><span class="sxs-lookup"><span data-stu-id="8faca-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="8faca-116">Si vous ne définissez pas le propriétaire sur **null**, la fenêtre parente continue à transmettre des messages à la fenêtre vidéo et des erreurs risquent de se produire au moment de la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="8faca-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8faca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8faca-117">Requirements</span></span>



| <span data-ttu-id="8faca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8faca-118">Requirement</span></span> | <span data-ttu-id="8faca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8faca-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8faca-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8faca-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8faca-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8faca-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8faca-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8faca-122">Library</span></span><br/> | <dl> <span data-ttu-id="8faca-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8faca-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8faca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8faca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8faca-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="8faca-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




