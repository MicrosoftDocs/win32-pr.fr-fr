---
description: La plupart des fonctionnalités de débogage décrites dans cette rubrique sont implémentées dans la bibliothèque de classes de base DirectShow. Pour plus d’informations, consultez classes de base DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Débogage des filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522556"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="57e71-104">Débogage des filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="57e71-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="57e71-105">La plupart des fonctionnalités de débogage décrites dans cette rubrique sont implémentées dans la bibliothèque de classes de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="57e71-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="57e71-106">Pour plus d’informations, consultez [classes de base DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="57e71-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="57e71-107">Vérification des assertions</span><span class="sxs-lookup"><span data-stu-id="57e71-107">Assertion Checking</span></span>

<span data-ttu-id="57e71-108">Utilisez la vérification d’assertion en toute libéralisation.</span><span class="sxs-lookup"><span data-stu-id="57e71-108">Use assertion checking liberally.</span></span> <span data-ttu-id="57e71-109">Les assertions peuvent vérifier les hypothèses que vous apportez dans votre code sur les conditions préalables et post-conditions.</span><span class="sxs-lookup"><span data-stu-id="57e71-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="57e71-110">DirectShow fournit plusieurs macros d’assertion.</span><span class="sxs-lookup"><span data-stu-id="57e71-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="57e71-111">Pour plus d’informations, consultez [macros Assert et Breakpoint](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="57e71-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="57e71-112">Noms d'objets</span><span class="sxs-lookup"><span data-stu-id="57e71-112">Object Names</span></span>

<span data-ttu-id="57e71-113">Dans les versions Debug, il existe une liste globale d’objets qui dérivent de la classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="57e71-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="57e71-114">À mesure que des objets sont créés, ils sont ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="57e71-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="57e71-115">Lorsqu’elles sont détruites, elles sont supprimées de la liste.</span><span class="sxs-lookup"><span data-stu-id="57e71-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="57e71-116">Pour afficher une liste de ces objets, appelez la fonction [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .</span><span class="sxs-lookup"><span data-stu-id="57e71-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="57e71-117">La méthode de constructeur pour la classe de base [**CBaseObject**](cbaseobject.md) , et la plupart des classes dérivées de celle-ci, comprend un paramètre pour le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57e71-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="57e71-118">Donnez à vos objets des noms uniques pour les identifier.</span><span class="sxs-lookup"><span data-stu-id="57e71-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="57e71-119">Utilisez la macro [**Name**](name.md) lorsque vous déclarez le nom, afin que le nom soit alloué uniquement dans les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="57e71-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="57e71-120">Dans les versions commerciales, le nom devient **null**.</span><span class="sxs-lookup"><span data-stu-id="57e71-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="57e71-121">Journalisation du débogage</span><span class="sxs-lookup"><span data-stu-id="57e71-121">Debug Logging</span></span>

<span data-ttu-id="57e71-122">La fonction [**DbgLog**](dbglog.md) affiche les messages de débogage au fur et à mesure de l’exécution de votre programme.</span><span class="sxs-lookup"><span data-stu-id="57e71-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="57e71-123">Utilisez cette fonction pour suivre l’exécution de votre application ou filtre.</span><span class="sxs-lookup"><span data-stu-id="57e71-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="57e71-124">Vous pouvez consigner les codes de retour, les valeurs des variables et toute autre information pertinente.</span><span class="sxs-lookup"><span data-stu-id="57e71-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="57e71-125">Chaque message de débogage a un type, tel que trace du journal \_ ou erreur de journal \_ , et un niveau de débogage, qui indique l’importance du message.</span><span class="sxs-lookup"><span data-stu-id="57e71-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="57e71-126">Les messages avec des niveaux de débogage inférieurs sont plus importants que ceux avec des niveaux supérieurs.</span><span class="sxs-lookup"><span data-stu-id="57e71-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="57e71-127">Dans l’exemple suivant, un filtre hypothétique déconnecte un code confidentiel d’un tableau de codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="57e71-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="57e71-128">Si la tentative de déconnexion a échoué, le filtre affiche un message de trace du journal \_ .</span><span class="sxs-lookup"><span data-stu-id="57e71-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="57e71-129">Si la tentative échoue, elle affiche un message d’erreur de journal \_ :</span><span class="sxs-lookup"><span data-stu-id="57e71-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="57e71-130">Lors du débogage, vous pouvez définir le niveau de débogage pour chaque type de message.</span><span class="sxs-lookup"><span data-stu-id="57e71-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="57e71-131">En outre, chaque module (DLL ou exécutable) conserve ses propres niveaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="57e71-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="57e71-132">Si vous testez un filtre, augmentez les niveaux de débogage de la DLL qui contient le filtre.</span><span class="sxs-lookup"><span data-stu-id="57e71-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="57e71-133">Pour plus d’informations, consultez [fonctions de sortie de débogage](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="57e71-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="57e71-134">Sections critiques</span><span class="sxs-lookup"><span data-stu-id="57e71-134">Critical Sections</span></span>

<span data-ttu-id="57e71-135">Pour faciliter le suivi des blocages, incluez des assertions qui déterminent si le code appelant possède une section critique donnée.</span><span class="sxs-lookup"><span data-stu-id="57e71-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="57e71-136">Les fonctions [**CritCheckIn**](critcheckin.md) et [**CritCheckOut**](critcheckout.md) indiquent si le thread appelant possède une section critique.</span><span class="sxs-lookup"><span data-stu-id="57e71-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="57e71-137">En général, vous appelez ces fonctions à partir d’une macro Assert.</span><span class="sxs-lookup"><span data-stu-id="57e71-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="57e71-138">Vous pouvez également utiliser la fonction [**DbgLockTrace**](dbglocktrace.md) pour tracer le moment où les sections critiques sont conservées ou libérées.</span><span class="sxs-lookup"><span data-stu-id="57e71-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e71-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57e71-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e71-140">Débogage dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="57e71-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



