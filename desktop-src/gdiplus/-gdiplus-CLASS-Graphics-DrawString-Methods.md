---
description: Cette rubrique répertorie les méthodes DrawString de la classe Graphics. Pour obtenir la liste complète des méthodes de la classe Graphics, consultez Graphics.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Méthodes Graphics. DrawString (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982994"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="86910-104">Graphics. DrawString, méthodes</span><span class="sxs-lookup"><span data-stu-id="86910-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="86910-105">Cette rubrique répertorie les méthodes DrawString de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="86910-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="86910-106">Pour obtenir la liste complète des méthodes de la classe **Graphics** , consultez [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="86910-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="86910-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="86910-107">Overload list</span></span>



| <span data-ttu-id="86910-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="86910-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="86910-109">Description</span><span class="sxs-lookup"><span data-stu-id="86910-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86910-110">[**DrawString (WCHAR \* , int, police \* , PointF&, Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="86910-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="86910-111">La méthode [**Graphics ::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) dessine une chaîne basée sur une police et une origine pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="86910-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="86910-112">[**DrawString (WCHAR \* , int, police \* , RectF&, StringFormat \* , Brush \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86910-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="86910-113">La méthode [**Graphics ::D rawstring**](/previous-versions//ms535991(v=vs.85)) dessine une chaîne basée sur une police, un rectangle de disposition et un format.</span><span class="sxs-lookup"><span data-stu-id="86910-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="86910-114">[**DrawString (WCHAR \* , int, police \* , PointF&, StringFormat \* , Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="86910-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="86910-115">La méthode [**Graphics ::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) dessine une chaîne basée sur une police, une origine de chaîne et un format.</span><span class="sxs-lookup"><span data-stu-id="86910-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="86910-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="86910-116">Requirements</span></span>



| <span data-ttu-id="86910-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86910-117">Requirement</span></span> | <span data-ttu-id="86910-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="86910-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86910-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="86910-119">Header</span></span><br/> | <dl> <span data-ttu-id="86910-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="86910-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
