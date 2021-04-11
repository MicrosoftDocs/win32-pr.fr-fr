---
description: Décrit comment utiliser les méthodes courantes des interfaces de collection.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Utilisation des interfaces de collection XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203468"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="57a62-103">Utilisation des interfaces de collection XPS OM</span><span class="sxs-lookup"><span data-stu-id="57a62-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="57a62-104">Décrit comment utiliser les méthodes courantes des interfaces de collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="57a62-105">Contenu</span><span class="sxs-lookup"><span data-stu-id="57a62-105">Contents</span></span>

<span data-ttu-id="57a62-106">Les méthodes décrites dans cette section s’affichent dans la liste qui suit.</span><span class="sxs-lookup"><span data-stu-id="57a62-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="57a62-107">Toutes les interfaces de collection ne prennent pas en charge chacune de ces méthodes, et certaines interfaces prennent également en charge les méthodes qui ne sont pas décrites dans cette page.</span><span class="sxs-lookup"><span data-stu-id="57a62-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="57a62-108">Pour obtenir la liste des méthodes prises en charge par une interface spécifique, reportez-vous à la description de la description de cette interface.</span><span class="sxs-lookup"><span data-stu-id="57a62-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="57a62-109">Append, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="57a62-110">GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="57a62-111">GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="57a62-112">Méthode InsertAt</span><span class="sxs-lookup"><span data-stu-id="57a62-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="57a62-113">RemoveAt, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="57a62-114">Méthode SetAt</span><span class="sxs-lookup"><span data-stu-id="57a62-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="57a62-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57a62-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="57a62-116">Append, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-116">Append Method</span></span>

<span data-ttu-id="57a62-117">Ajoute un objet à la fin de la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="57a62-118">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="57a62-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-119">**Description**</span></span>

<span data-ttu-id="57a62-120">À la fin de la collection, cette méthode ajoute un objet qui est passé dans la liste de paramètres, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="57a62-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![figure qui montre comment Append ajoute une entrée à la collection](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="57a62-122">GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-122">GetAt Method</span></span>

<span data-ttu-id="57a62-123">Obtient un objet à partir d’un emplacement spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="57a62-124">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="57a62-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-125">**Description**</span></span>

<span data-ttu-id="57a62-126">Écrit l’objet qui est stocké à l’emplacement de la collection spécifié par *index* à la variable référencée par l' *objet*.</span><span class="sxs-lookup"><span data-stu-id="57a62-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="57a62-127">Cette action ne modifie pas le contenu de la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="57a62-128">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="57a62-128">The following diagram illustrates this process.</span></span>

![figure qui montre comment GetAt récupère une entrée de la collection](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="57a62-130">GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-130">GetCount Method</span></span>

<span data-ttu-id="57a62-131">Obtient le nombre d’objets stockés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="57a62-132">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="57a62-133">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-133">**Description**</span></span>

<span data-ttu-id="57a62-134">Écrit le nombre d’objets actuellement stockés dans la collection dans la variable référencée par *Count*.</span><span class="sxs-lookup"><span data-stu-id="57a62-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="57a62-135">Cette action ne modifie pas le contenu de la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="57a62-136">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="57a62-136">The following diagram illustrates this process.</span></span>

![figure qui montre comment GetCount obtient le nombre d’entrées dans la collection](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="57a62-138">Méthode InsertAt</span><span class="sxs-lookup"><span data-stu-id="57a62-138">InsertAt Method</span></span>

<span data-ttu-id="57a62-139">Insère un objet à l’emplacement spécifié de la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="57a62-140">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="57a62-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-141">**Description**</span></span>

<span data-ttu-id="57a62-142">L’objet qui est passé dans l' *objet* est inséré dans la collection à l’emplacement spécifié par l' *index*.</span><span class="sxs-lookup"><span data-stu-id="57a62-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="57a62-143">Avant d’insérer le nouvel *objet*, cette méthode se déplace de 1 l’objet qui a occupé l’emplacement au niveau de l' *index* et déplace tous les pointeurs d’interface après l' *index*.</span><span class="sxs-lookup"><span data-stu-id="57a62-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="57a62-144">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="57a62-144">The following diagram illustrates this process.</span></span>

![figure qui montre comment InsertAt ajoute une entrée à la collection](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="57a62-146">RemoveAt, méthode</span><span class="sxs-lookup"><span data-stu-id="57a62-146">RemoveAt Method</span></span>

<span data-ttu-id="57a62-147">Supprime l’objet à partir d’un emplacement spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="57a62-148">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="57a62-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-149">**Description**</span></span>

<span data-ttu-id="57a62-150">Cette méthode libère l’objet à partir de l’emplacement spécifié par *index*, puis compacte la collection en réduisant de 1 l’index de chaque pointeur à la suite de l' *index*.</span><span class="sxs-lookup"><span data-stu-id="57a62-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="57a62-151">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="57a62-151">The following diagram illustrates this process.</span></span>

![figure qui montre comment RemoveAt supprime une entrée de la collection](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="57a62-153">Méthode SetAt</span><span class="sxs-lookup"><span data-stu-id="57a62-153">SetAt Method</span></span>

<span data-ttu-id="57a62-154">Remplace l’objet à un emplacement spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="57a62-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="57a62-155">**Syntaxe générique**</span><span class="sxs-lookup"><span data-stu-id="57a62-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="57a62-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="57a62-156">**Description**</span></span>

<span data-ttu-id="57a62-157">Cette méthode libère d’abord l’objet à l’emplacement référencé par l' *index*, puis remplace cet objet par celui qui est passé dans l' *objet*.</span><span class="sxs-lookup"><span data-stu-id="57a62-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="57a62-158">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="57a62-158">The following diagram illustrates this process.</span></span>

![figure qui montre comment setat remplace une entrée dans la collection](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="57a62-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57a62-160">See Also</span></span>

<dl>

[<span data-ttu-id="57a62-161">**IXpsOMColorProfileResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="57a62-162">**IXpsOMDashCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="57a62-163">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="57a62-164">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="57a62-165">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="57a62-166">**IXpsOMGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="57a62-167">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="57a62-168">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="57a62-169">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="57a62-170">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="57a62-171">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="57a62-172">**IXpsOMSignatureBlockResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="57a62-173">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="57a62-174">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="57a62-175">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="57a62-176">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="57a62-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



