---
description: Gestion des erreurs d’administration COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Gestion des erreurs d’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519219"
---
# <a name="handling-com-administration-errors"></a><span data-ttu-id="d8640-103">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="d8640-103">Handling COM+ Administration Errors</span></span>

<span data-ttu-id="d8640-104">Les erreurs générées lors de l’utilisation des objets comadmin sont signalées de deux manières, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d8640-104">Errors that are generated when using the COMAdmin objects are reported in two ways, as follows:</span></span>

-   <span data-ttu-id="d8640-105">Utilisation de codes d’erreur spécifiques à la bibliothèque comadmin.</span><span class="sxs-lookup"><span data-stu-id="d8640-105">Using error codes specific to the COMAdmin library.</span></span>
-   <span data-ttu-id="d8640-106">Utilisation des informations d’erreur étendues disponibles dans une collection [**errorInfo**](errorinfo.md) spéciale.</span><span class="sxs-lookup"><span data-stu-id="d8640-106">Using extended error information available in a special [**ErrorInfo**](errorinfo.md) collection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8640-107">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d8640-107">Error Codes</span></span>

<span data-ttu-id="d8640-108">Vous gérez les codes d’erreur d’administration comme vous le feriez pour n’importe quel message d’erreur COM.</span><span class="sxs-lookup"><span data-stu-id="d8640-108">You handle administration error codes as you would any COM error message.</span></span> <span data-ttu-id="d8640-109">Dans Microsoft Visual C++, ces codes sont retournés en tant que valeurs **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8640-109">In Microsoft Visual C++, these codes are returned as **HRESULT** values.</span></span> <span data-ttu-id="d8640-110">Dans Microsoft Visual Basic, elles sont levées en tant qu’exceptions que vous pouvez intercepter.</span><span class="sxs-lookup"><span data-stu-id="d8640-110">In Microsoft Visual Basic, they are thrown as exceptions that you can catch.</span></span> <span data-ttu-id="d8640-111">Pour les programmeurs C++, les codes d’erreur d’administration COM+ sont définis dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d8640-111">For C++ programmers, the COM+ administration error codes are defined in Winerror.h.</span></span> <span data-ttu-id="d8640-112">Pour les programmeurs Visual Basic, ils sont disponibles via l’IDE Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d8640-112">For Visual Basic programmers, they are available through the Visual Basic IDE.</span></span>

## <a name="errorinfo-collection"></a><span data-ttu-id="d8640-113">ErrorInfo, collection</span><span class="sxs-lookup"><span data-stu-id="d8640-113">ErrorInfo Collection</span></span>

<span data-ttu-id="d8640-114">Lorsqu’une erreur se produit, signalée par un code d’échec, des informations plus détaillées peuvent être disponibles, en fonction de la nature de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8640-114">When an error occurs, signaled by some kind of failure code, more detailed information may be available, depending on the nature of the error.</span></span> <span data-ttu-id="d8640-115">Les objets comadmin fournissent des informations étendues dans les cas où la cause précise de l’échec est difficile à déterminer sans rapport détaillé, par exemple avec plusieurs opérations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="d8640-115">The COMAdmin objects provide extended information in circumstances where the precise cause of the failure is difficult to determine without a detailed report, such as with multiple read and write operations.</span></span>

<span data-ttu-id="d8640-116">Par exemple, lorsque vous utilisez des méthodes telles que [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur un objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , vous pouvez lire ou écrire des données pour chaque élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="d8640-116">For example, when you use methods such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, you can be reading or writing data for every item in the collection.</span></span> <span data-ttu-id="d8640-117">Des erreurs compliquées peuvent se produire, et elles peuvent être difficiles à diagnostiquer en fonction d’un code d’erreur numérique unique.</span><span class="sxs-lookup"><span data-stu-id="d8640-117">Complicated errors can occur, and they can be difficult to diagnose based on a single numeric error code.</span></span> <span data-ttu-id="d8640-118">Par conséquent, la bibliothèque comadmin génère des informations d’erreur étendues par le biais d’une collection spéciale.</span><span class="sxs-lookup"><span data-stu-id="d8640-118">Therefore, the COMAdmin Library makes extended error information through a special collection.</span></span>

<span data-ttu-id="d8640-119">Quand des informations d’erreur étendues sont disponibles, elles sont placées dans la collection [**errorInfo**](errorinfo.md) qui est associée à la collection d’origine qui a rencontré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8640-119">When extended error information is available, it is placed in the [**ErrorInfo**](errorinfo.md) collection that is related to the original collection that had the error.</span></span> <span data-ttu-id="d8640-120">Pour récupérer le rapport d’erreurs, récupérez la collection **errorInfo** qui est associée à la collection d’origine et examinez les éléments qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="d8640-120">To retrieve the error report, get the **ErrorInfo** collection that is related to the original collection and examine the items it contains.</span></span> <span data-ttu-id="d8640-121">Vous pouvez récupérer la collection **errorInfo** à l’aide de [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur [**COMAdminCatalogCollection**](comadmincatalogcollection.md), en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.</span><span class="sxs-lookup"><span data-stu-id="d8640-121">You can retrieve the **ErrorInfo** collection by using [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on [**COMAdminCatalogCollection**](comadmincatalogcollection.md), leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

<span data-ttu-id="d8640-122">Quand vous recevez une erreur, vous devez immédiatement obtenir et remplir la collection [**errorInfo**](errorinfo.md) pour la collection qui a échoué, sans effectuer d’autres opérations sur cette collection.</span><span class="sxs-lookup"><span data-stu-id="d8640-122">When you get an error, you must immediately get and populate the [**ErrorInfo**](errorinfo.md) collection for the collection that failed, without performing any other operations on that collection.</span></span> <span data-ttu-id="d8640-123">Dans le cas contraire, la collection **errorInfo** est réinitialisée et ne détaille pas cette erreur.</span><span class="sxs-lookup"><span data-stu-id="d8640-123">Otherwise, the **ErrorInfo** collection is reset and does not detail that failure.</span></span>

<span data-ttu-id="d8640-124">Les éléments de la collection [**errorInfo**](errorinfo.md) exposent les propriétés spéciales de signalement d’erreurs MajorRef et MinorRef, qui détaillent la cause particulière de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8640-124">The items in the [**ErrorInfo**](errorinfo.md) collection expose the special error-reporting properties MajorRef and MinorRef, which detail the particular cause of the error.</span></span> <span data-ttu-id="d8640-125">Pour plus d’informations, consultez **errorInfo**.</span><span class="sxs-lookup"><span data-stu-id="d8640-125">For more information, see **ErrorInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8640-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8640-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8640-127">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="d8640-127">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="d8640-128">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="d8640-128">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="d8640-129">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="d8640-129">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="d8640-130">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="d8640-130">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="d8640-131">Définition des propriétés et enregistrement des modifications dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="d8640-131">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



