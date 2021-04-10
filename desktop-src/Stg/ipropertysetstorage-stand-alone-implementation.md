---
title: IPropertySetStorage-implémentation autonome
description: L’implémentation autonome fournie par le système de IPropertySetStorage comprend une implémentation de IPropertyStorage et IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implémentations
- IPropertySetStorage Strctd STG, implémentations, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031347"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="8b0e1-105">IPropertySetStorage-implémentation autonome</span><span class="sxs-lookup"><span data-stu-id="8b0e1-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="8b0e1-106">L’implémentation autonome fournie par le système de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) comprend une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) est l’interface qui lit et écrit les propriétés dans un stockage de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="8b0e1-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) est l’interface qui crée et ouvre les jeux de propriétés dans un stockage.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="8b0e1-108">Les interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) et [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sont également fournies dans l’implémentation autonome.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="8b0e1-109">Pour utiliser l’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), obtenez d’abord un pointeur vers l’implémentation fournie par le système et autonome, et associez l’implémentation fournie par le système à votre objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="8b0e1-110">Pour obtenir un pointeur vers l’implémentation autonome de **IPropertySetStorage**, appelez la fonction [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) et fournissez le paramètre *pStorage* en spécifiant l’objet de stockage qui contiendra le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="8b0e1-111">Cette fonction fournit un pointeur vers la nouvelle interface **IPropertySetStorage** pour l’objet de stockage spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="8b0e1-112">L’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crée des jeux de propriétés sur n’importe quel objet de stockage, pas seulement sur des stockages de fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="8b0e1-113">L’implémentation autonome ne dépend pas de fichiers composés et peut être utilisée avec n’importe quelle implémentation de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="8b0e1-114">Toutes les restrictions sur les stockages structurés fournis par l’appelant s’appliquent à cette implémentation des jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="8b0e1-115">Par exemple, si vous fournissez un stockage en mode simple à [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), le **IPropertySetStorage** résultant sera limité par l' [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fourni.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="8b0e1-116">Pour plus d’informations sur l’implémentation de fichier composé de cette interface, consultez la section [IPropertySetStorage-Implementation file Implementation](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="8b0e1-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="8b0e1-117">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="8b0e1-117">When to Use</span></span>

<span data-ttu-id="8b0e1-118">Appelez les méthodes de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour créer, ouvrir et supprimer des jeux de propriétés dans tout stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="8b0e1-119">Il existe également une méthode qui fournit un pointeur vers l’énumérateur [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) qui peut être utilisé pour énumérer les jeux de propriétés dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="8b0e1-120">L’implémentation autonome fournit également les fonctions d’assistance [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) et [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , en plus des méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , pour créer et ouvrir des jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="8b0e1-121">Ces deux fonctions ajoutent la prise en charge de la \_ valeur non mise en mémoire tampon PROPSETFLAG afin que vous puissiez écrire les modifications directement dans le jeu de propriétés au lieu de les mettre en mémoire tampon dans un cache.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="8b0e1-122">Pour plus d’informations, consultez [**constantes PROPSETFLAG**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8b0e1-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="8b0e1-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b0e1-123">Methods</span></span>

<span data-ttu-id="8b0e1-124">L’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="8b0e1-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="8b0e1-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="8b0e1-126">Crée un nouveau jeu de propriétés dans le stockage et retourne un pointeur vers l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="8b0e1-127">Si vous envisagez d’utiliser la \_ valeur non mise en mémoire tampon PROPSETFLAG, utilisez la fonction [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) à la place pour créer et ouvrir le nouveau jeu de propriétés et pour obtenir un pointeur vers l’implémentation autonome de l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e1-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="8b0e1-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="8b0e1-129">Ouvre un jeu de propriétés existant dans le stockage et retourne un pointeur vers l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="8b0e1-130">Si vous envisagez d’utiliser la \_ valeur non mise en mémoire tampon PROPSETFLAG, utilisez la fonction [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) à la place pour obtenir un pointeur vers l’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e1-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage ::D supprim**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="8b0e1-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="8b0e1-132">Supprime un jeu de propriétés dans ce jeu de propriétés stockage.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e1-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="8b0e1-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="8b0e1-134">Crée un objet qui peut être utilisé pour énumérer des structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) .</span><span class="sxs-lookup"><span data-stu-id="8b0e1-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="8b0e1-135">Chaque structure **STATPROPSETSTG** fournit des données relatives à un jeu de propriétés unique.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="8b0e1-136">La propriété DocumentSummaryInformation et UserDefined définie est unique en ce qu’elle peut avoir deux sections de jeu de propriétés dans un seul flux sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8b0e1-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="8b0e1-137">Pour plus d’informations, consultez [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="8b0e1-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8b0e1-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b0e1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b0e1-139">IPropertyStorage-implémentation autonome</span><span class="sxs-lookup"><span data-stu-id="8b0e1-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="8b0e1-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="8b0e1-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="8b0e1-142">**IStorage :: EnumElements**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="8b0e1-143">**Constantes PROPSETFLAG**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="8b0e1-144">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="8b0e1-145">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="8b0e1-146">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="8b0e1-147">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="8b0e1-148">**Constantes STGM**</span><span class="sxs-lookup"><span data-stu-id="8b0e1-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 