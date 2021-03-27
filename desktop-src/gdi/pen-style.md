---
description: L’attribut style spécifie le motif de ligne qui apparaît lorsqu’un stylet cosmétique ou géométrique particulier est utilisé. Il existe huit styles de stylet prédéfinis. L’illustration suivante montre les sept de ces styles qui sont définis par le système.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Style de stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951552"
---
# <a name="pen-style"></a><span data-ttu-id="f7da0-105">Style de stylet</span><span class="sxs-lookup"><span data-stu-id="f7da0-105">Pen Style</span></span>

<span data-ttu-id="f7da0-106">L’attribut style spécifie le motif de ligne qui apparaît lorsqu’un stylet cosmétique ou géométrique particulier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f7da0-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="f7da0-107">Il existe huit styles de stylet prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="f7da0-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="f7da0-108">L’illustration suivante montre les sept de ces styles qui sont définis par le système.</span><span class="sxs-lookup"><span data-stu-id="f7da0-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![Illustration montrant sept lignes, chacune d’elles étant dessinée à l’aide d’un style prédéfini différent](images/cspen-01.png)

<span data-ttu-id="f7da0-110">Le style de cadre intérieur est identique au style plein pour les plumes cosmétiques.</span><span class="sxs-lookup"><span data-stu-id="f7da0-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="f7da0-111">Toutefois, elle fonctionne différemment lorsqu’elle est utilisée avec un stylet géométrique.</span><span class="sxs-lookup"><span data-stu-id="f7da0-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="f7da0-112">Si le stylet géométrique est plus grand qu’un pixel unique et qu’une fonction de dessin utilise le stylet pour dessiner une bordure autour d’un objet rempli, le système dessine la bordure à l’intérieur du cadre de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f7da0-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="f7da0-113">En utilisant le style d’image interne, une application peut garantir qu’un objet apparaît entièrement dans les dimensions spécifiées, quelle que soit la largeur géométrique du stylet.</span><span class="sxs-lookup"><span data-stu-id="f7da0-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="f7da0-114">Outre les sept styles définis par le système, il existe un huitième style qui est défini par l’utilisateur (ou l’application).</span><span class="sxs-lookup"><span data-stu-id="f7da0-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="f7da0-115">Un style défini par l’utilisateur génère des lignes avec une série personnalisée de tirets et de points.</span><span class="sxs-lookup"><span data-stu-id="f7da0-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="f7da0-116">Utilisez la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) pour créer un stylet avec les styles définis par le système.</span><span class="sxs-lookup"><span data-stu-id="f7da0-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="f7da0-117">Utilisez la fonction **ExtCreatePen** pour créer un stylet avec un style défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7da0-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



