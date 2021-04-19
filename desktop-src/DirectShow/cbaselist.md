---
description: La méthode CBaseList implémente une liste ABTRACT. Le modèle de classe CGenericList, qui dérive de CBaseList, fournit la vérification de type et une interface plus simple que la classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: CBaseList, classe (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539583"
---
# <a name="cbaselist-class"></a><span data-ttu-id="40c3b-104">CBaseList, classe</span><span class="sxs-lookup"><span data-stu-id="40c3b-104">CBaseList class</span></span>

![hiérarchie de la classe cbaselist](images/list01.png)

<span data-ttu-id="40c3b-106">La méthode **CBaseList** implémente une liste ABTRACT.</span><span class="sxs-lookup"><span data-stu-id="40c3b-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="40c3b-107">Le modèle de classe [**CGenericList**](cgenericlist.md) , qui dérive de **CBaseList**, fournit la vérification de type et une interface plus simple que la classe **CBaseList** .</span><span class="sxs-lookup"><span data-stu-id="40c3b-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="40c3b-108">La classe **CBaseList** est modélisée après la classe **CObList** dans la bibliothèque Microsoft Foundation classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="40c3b-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="40c3b-109">Les positions dans la liste sont représentées par une structure de POSITION.</span><span class="sxs-lookup"><span data-stu-id="40c3b-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="40c3b-110">L’appelant ne doit pas accéder aux membres internes de la structure de POSITION ; le traiter en tant que pointeur vers un nœud de liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="40c3b-111">La position d’un objet dans la liste reste valide jusqu’à ce que l’objet soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="40c3b-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="40c3b-112">La liste ne nécessite aucune prise en charge par les objets qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="40c3b-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="40c3b-113">Il n’effectue aucune gestion du stockage ou copie sur les objets.</span><span class="sxs-lookup"><span data-stu-id="40c3b-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="40c3b-114">Les objets peuvent figurer dans plusieurs listes.</span><span class="sxs-lookup"><span data-stu-id="40c3b-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="40c3b-115">Environ la moitié des méthodes de cette classe agissent sur des objets uniques.</span><span class="sxs-lookup"><span data-stu-id="40c3b-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="40c3b-116">Ces méthodes ont le suffixe-I dans le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="40c3b-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="40c3b-117">Les autres méthodes agissent sur des listes entières.</span><span class="sxs-lookup"><span data-stu-id="40c3b-117">The other methods act on entire lists.</span></span> <span data-ttu-id="40c3b-118">Par exemple, la méthode [**CBaseList :: AddAfter**](cbaselist-addafter.md) ajoute une liste à une autre liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="40c3b-119">Les opérations à objet unique retournent des valeurs de POSITION, ou **null** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="40c3b-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="40c3b-120">Les opérations de liste retournent **true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="40c3b-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="40c3b-121">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="40c3b-121">Protected Member Variables</span></span>                             | <span data-ttu-id="40c3b-122">Description</span><span class="sxs-lookup"><span data-stu-id="40c3b-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="40c3b-123">**\_nombre m**</span><span class="sxs-lookup"><span data-stu-id="40c3b-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="40c3b-124">Nombre d’éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="40c3b-125">**m \_ pFirst**</span><span class="sxs-lookup"><span data-stu-id="40c3b-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="40c3b-126">Pointeur vers le premier nœud de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="40c3b-127">**m \_ pLast**</span><span class="sxs-lookup"><span data-stu-id="40c3b-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="40c3b-128">Pointeur vers le dernier nœud de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="40c3b-129">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="40c3b-129">Protected Methods</span></span>                                      | <span data-ttu-id="40c3b-130">Description</span><span class="sxs-lookup"><span data-stu-id="40c3b-130">Description</span></span>                                                               |
| [<span data-ttu-id="40c3b-131">**GetNextI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="40c3b-132">Récupère l’élément à la position spécifiée et avance la position.</span><span class="sxs-lookup"><span data-stu-id="40c3b-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="40c3b-133">**GetI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="40c3b-134">Récupère l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="40c3b-135">**Rechercher**</span><span class="sxs-lookup"><span data-stu-id="40c3b-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="40c3b-136">Récupère la première position qui contient l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="40c3b-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="40c3b-137">**RemoveHeadI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="40c3b-138">Supprime le premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="40c3b-139">**RemoveTailI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="40c3b-140">Supprime le dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="40c3b-141">**Supprimeri**</span><span class="sxs-lookup"><span data-stu-id="40c3b-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="40c3b-142">Supprime l'élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="40c3b-143">**AddTailI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="40c3b-144">Ajoute un élément à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="40c3b-145">**AddHeadI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="40c3b-146">Ajoute un élément au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="40c3b-147">**AddAfterI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="40c3b-148">Insère un élément après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="40c3b-149">**AddBeforeI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="40c3b-150">Insère un élément avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="40c3b-151">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="40c3b-151">Public Methods</span></span>                                         | <span data-ttu-id="40c3b-152">Description</span><span class="sxs-lookup"><span data-stu-id="40c3b-152">Description</span></span>                                                               |
| [<span data-ttu-id="40c3b-153">**CBaseList**</span><span class="sxs-lookup"><span data-stu-id="40c3b-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="40c3b-154">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="40c3b-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="40c3b-155">**~ CBaseList**</span><span class="sxs-lookup"><span data-stu-id="40c3b-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="40c3b-156">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="40c3b-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="40c3b-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="40c3b-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="40c3b-158">Supprime tous les nœuds de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="40c3b-159">**GetHeadPositionI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="40c3b-160">Récupère la position du premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="40c3b-161">**GetTailPositionI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="40c3b-162">Récupère la position du dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="40c3b-163">**GetCountI**</span><span class="sxs-lookup"><span data-stu-id="40c3b-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="40c3b-164">Récupère le nombre d’éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="40c3b-165">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="40c3b-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="40c3b-166">Récupère la position suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="40c3b-167">**PREV**</span><span class="sxs-lookup"><span data-stu-id="40c3b-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="40c3b-168">Récupère la position précédente dans la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="40c3b-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="40c3b-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="40c3b-170">Insère une autre liste au début de cette liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="40c3b-171">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="40c3b-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="40c3b-172">Ajoute une autre liste à la fin de cette liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="40c3b-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="40c3b-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="40c3b-174">Insère une liste après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="40c3b-175">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="40c3b-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="40c3b-176">Insère une liste avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40c3b-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="40c3b-177">**MoveToTail**</span><span class="sxs-lookup"><span data-stu-id="40c3b-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="40c3b-178">Fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="40c3b-179">**MoveToHead**</span><span class="sxs-lookup"><span data-stu-id="40c3b-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="40c3b-180">Divise la liste et insère la partie de la fin à l’en-tête d’une autre liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="40c3b-181">**TVA**</span><span class="sxs-lookup"><span data-stu-id="40c3b-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="40c3b-182">Inverse l’ordre de la liste.</span><span class="sxs-lookup"><span data-stu-id="40c3b-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="40c3b-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40c3b-183">Requirements</span></span>



| <span data-ttu-id="40c3b-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40c3b-184">Requirement</span></span> | <span data-ttu-id="40c3b-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="40c3b-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c3b-186">En-tête</span><span class="sxs-lookup"><span data-stu-id="40c3b-186">Header</span></span><br/>  | <dl> <span data-ttu-id="40c3b-187"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40c3b-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40c3b-188">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40c3b-188">Library</span></span><br/> | <dl> <span data-ttu-id="40c3b-189"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="40c3b-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c3b-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c3b-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c3b-191">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="40c3b-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




