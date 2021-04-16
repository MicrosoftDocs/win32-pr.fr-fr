---
description: L’objet DivisionResult représente un instantané de l’analyse de la disposition des traits contenus dans l’objet diviseur. Il contient la classification des traits et les informations de regroupement de l’analyse de la disposition.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Utilisation de l’objet DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526889"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="f5f3c-104">Utilisation de l’objet DivisionResult</span><span class="sxs-lookup"><span data-stu-id="f5f3c-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="f5f3c-105">L’objet **DivisionResult** représente un instantané de l’analyse de la disposition des traits contenus dans l’objet **diviseur** .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="f5f3c-106">Il contient la classification des traits et les informations de regroupement de l’analyse de la disposition.</span><span class="sxs-lookup"><span data-stu-id="f5f3c-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="f5f3c-107">Vous pouvez récupérer des informations à partir de l’objet **DivisionResult** par type d’élément structurel, tel que le dessin ou les lignes d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="f5f3c-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="f5f3c-108">L’objet **DivisionResult** peut être conservé après la destruction de l’objet **diviseur** .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="f5f3c-109">Dans Automation, cet objet est appelé objet d' [**interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="f5f3c-110">La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) de l’objet **DivisionResult** contient une copie de la collection **Strokes** dans l’objet **diviseur** au moment de la création de l’objet **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="f5f3c-111">L’énumération [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) définit les types d’éléments structurels reconnus par l’analyse de la disposition.</span><span class="sxs-lookup"><span data-stu-id="f5f3c-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="f5f3c-112">La méthode [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) de l’objet **DivisionResult** retourne une collection **DivisionUnits** qui contient tous les éléments structurels d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="f5f3c-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="f5f3c-113">Un élément structurel individuel est représenté par un objet **DivisionUnit** .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="f5f3c-114">Chaque fois que vous appelez la méthode **ResultByType** , l’objet **DivisionResult** crée une collection **DivisionUnits** .</span><span class="sxs-lookup"><span data-stu-id="f5f3c-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="f5f3c-115">Pour plus d’informations sur l’objet **DivisionUnit** , consultez [utilisation de l’objet DivisionUnit](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="f5f3c-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
