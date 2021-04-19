---
description: La méthode UOPValid récupère une valeur qui indique si l’opération utilisateur spécifiée (UOP) est actuellement valide.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Méthode UOPValid (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537441"
---
# <a name="uopvalid-method"></a><span data-ttu-id="45ff7-103">Méthode UOPValid</span><span class="sxs-lookup"><span data-stu-id="45ff7-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="45ff7-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="45ff7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="45ff7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="45ff7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="45ff7-106">La `UOPValid` méthode récupère une valeur qui indique si l’opération utilisateur spécifiée (UOP) est actuellement valide.</span><span class="sxs-lookup"><span data-stu-id="45ff7-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="45ff7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45ff7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ff7-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span><span class="sxs-lookup"><span data-stu-id="45ff7-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="45ff7-109">Spécifie l’opération de l’utilisateur (UOP) sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="45ff7-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="45ff7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="45ff7-110">Value</span></span> | <span data-ttu-id="45ff7-111">Description</span><span class="sxs-lookup"><span data-stu-id="45ff7-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ff7-112">0</span><span class="sxs-lookup"><span data-stu-id="45ff7-112">0</span></span>     | <span data-ttu-id="45ff7-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="45ff7-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="45ff7-114">1</span><span class="sxs-lookup"><span data-stu-id="45ff7-114">1</span></span>     | [<span data-ttu-id="45ff7-115">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="45ff7-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="45ff7-116">2</span><span class="sxs-lookup"><span data-stu-id="45ff7-116">2</span></span>     | [<span data-ttu-id="45ff7-117">**PlayTitle**</span><span class="sxs-lookup"><span data-stu-id="45ff7-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="45ff7-118">3</span><span class="sxs-lookup"><span data-stu-id="45ff7-118">3</span></span>     | [<span data-ttu-id="45ff7-119">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="45ff7-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="45ff7-120">4</span><span class="sxs-lookup"><span data-stu-id="45ff7-120">4</span></span>     | [<span data-ttu-id="45ff7-121">**ReturnFromSubmenu**</span><span class="sxs-lookup"><span data-stu-id="45ff7-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="45ff7-122">5</span><span class="sxs-lookup"><span data-stu-id="45ff7-122">5</span></span>     | [<span data-ttu-id="45ff7-123">**PlayChapter**</span><span class="sxs-lookup"><span data-stu-id="45ff7-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="45ff7-124">6</span><span class="sxs-lookup"><span data-stu-id="45ff7-124">6</span></span>     | <span data-ttu-id="45ff7-125">[**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="45ff7-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="45ff7-126">7</span><span class="sxs-lookup"><span data-stu-id="45ff7-126">7</span></span>     | [<span data-ttu-id="45ff7-127">**PlayNextChapter**</span><span class="sxs-lookup"><span data-stu-id="45ff7-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="45ff7-128">8</span><span class="sxs-lookup"><span data-stu-id="45ff7-128">8</span></span>     | [<span data-ttu-id="45ff7-129">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="45ff7-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="45ff7-130">9</span><span class="sxs-lookup"><span data-stu-id="45ff7-130">9</span></span>     | [<span data-ttu-id="45ff7-131">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="45ff7-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="45ff7-132">10</span><span class="sxs-lookup"><span data-stu-id="45ff7-132">10</span></span>    | <span data-ttu-id="45ff7-133">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 2 ( \_ titre de menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="45ff7-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="45ff7-134">11</span><span class="sxs-lookup"><span data-stu-id="45ff7-134">11</span></span>    | <span data-ttu-id="45ff7-135">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 3 ( \_ racine du menu du DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="45ff7-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="45ff7-136">12</span><span class="sxs-lookup"><span data-stu-id="45ff7-136">12</span></span>    | <span data-ttu-id="45ff7-137">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 4 ( \_ sous-image du menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="45ff7-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="45ff7-138">13</span><span class="sxs-lookup"><span data-stu-id="45ff7-138">13</span></span>    | <span data-ttu-id="45ff7-139">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 5 ( \_ menu DVD \_ audio)</span><span class="sxs-lookup"><span data-stu-id="45ff7-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="45ff7-140">14</span><span class="sxs-lookup"><span data-stu-id="45ff7-140">14</span></span>    | <span data-ttu-id="45ff7-141">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 6 ( \_ angle de menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="45ff7-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="45ff7-142">15</span><span class="sxs-lookup"><span data-stu-id="45ff7-142">15</span></span>    | <span data-ttu-id="45ff7-143">[**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 7 ( \_ chapitre du menu DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="45ff7-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="45ff7-144">16</span><span class="sxs-lookup"><span data-stu-id="45ff7-144">16</span></span>    | [<span data-ttu-id="45ff7-145">**Sort**</span><span class="sxs-lookup"><span data-stu-id="45ff7-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="45ff7-146">17</span><span class="sxs-lookup"><span data-stu-id="45ff7-146">17</span></span>    | <span data-ttu-id="45ff7-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="45ff7-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="45ff7-148">18</span><span class="sxs-lookup"><span data-stu-id="45ff7-148">18</span></span>    | [<span data-ttu-id="45ff7-149">**StillOff**</span><span class="sxs-lookup"><span data-stu-id="45ff7-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="45ff7-150">19</span><span class="sxs-lookup"><span data-stu-id="45ff7-150">19</span></span>    | [<span data-ttu-id="45ff7-151">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="45ff7-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="45ff7-152">20</span><span class="sxs-lookup"><span data-stu-id="45ff7-152">20</span></span>    | [<span data-ttu-id="45ff7-153">**CurrentAudioStream**</span><span class="sxs-lookup"><span data-stu-id="45ff7-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="45ff7-154">21</span><span class="sxs-lookup"><span data-stu-id="45ff7-154">21</span></span>    | [<span data-ttu-id="45ff7-155">**CurrentSubpictureStream**</span><span class="sxs-lookup"><span data-stu-id="45ff7-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="45ff7-156">22</span><span class="sxs-lookup"><span data-stu-id="45ff7-156">22</span></span>    | <span data-ttu-id="45ff7-157">[**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="45ff7-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="45ff7-158">23</span><span class="sxs-lookup"><span data-stu-id="45ff7-158">23</span></span>    | [<span data-ttu-id="45ff7-159">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="45ff7-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="45ff7-160">24</span><span class="sxs-lookup"><span data-stu-id="45ff7-160">24</span></span>    | <span data-ttu-id="45ff7-161">Sélectionnez préférence du mode vidéo.</span><span class="sxs-lookup"><span data-stu-id="45ff7-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ff7-162">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45ff7-162">Return Value</span></span>

<span data-ttu-id="45ff7-163">Retourne une valeur booléenne indiquant si l’opération spécifiée est autorisée par le contrôle UOP.</span><span class="sxs-lookup"><span data-stu-id="45ff7-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ff7-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45ff7-164">Requirements</span></span>



| <span data-ttu-id="45ff7-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45ff7-165">Requirement</span></span> | <span data-ttu-id="45ff7-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="45ff7-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45ff7-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="45ff7-167">Header</span></span><br/> | <dl> <span data-ttu-id="45ff7-168"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="45ff7-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




