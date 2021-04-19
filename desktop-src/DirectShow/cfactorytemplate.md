---
description: Fournit un modèle pour créer des fabriques de classes.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: CFactoryTemplate, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537990"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="354ab-103">CFactoryTemplate, classe</span><span class="sxs-lookup"><span data-stu-id="354ab-103">CFactoryTemplate class</span></span>

<span data-ttu-id="354ab-104">Fournit un modèle pour créer des fabriques de classes.</span><span class="sxs-lookup"><span data-stu-id="354ab-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="354ab-105">Dans DirectShow, les fabriques de classes sont spécialisées à l’aide de la classe **CFactoryTemplate** , également appelée *modèle de fabrique*.</span><span class="sxs-lookup"><span data-stu-id="354ab-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="354ab-106">Chaque fabrique de classe contient un pointeur vers un modèle de fabrique.</span><span class="sxs-lookup"><span data-stu-id="354ab-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="354ab-107">Le modèle de fabrique contient des informations sur un objet COM, y compris l’identificateur de classe (CLSID) de l’objet et un pointeur vers une fonction qui crée l’objet.</span><span class="sxs-lookup"><span data-stu-id="354ab-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="354ab-108">Dans votre DLL, déclarez un tableau global de modèles de fabrique nommés *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="354ab-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="354ab-109">Incluez un modèle de fabrique pour chaque objet dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="354ab-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="354ab-110">Quand la fonction [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crée une nouvelle fabrique de classes, elle recherche un modèle avec un CLSID correspondant dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="354ab-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="354ab-111">En supposant qu’il en trouve un, il crée une fabrique de classe qui contient un pointeur vers le modèle correspondant.</span><span class="sxs-lookup"><span data-stu-id="354ab-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="354ab-112">Lorsque le client appelle **IClassFactory :: CreateInstance**, la fabrique de classe appelle la fonction d’instanciation définie dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="354ab-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="354ab-113">Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="354ab-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="354ab-114">Variables membres publiques</span><span class="sxs-lookup"><span data-stu-id="354ab-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="354ab-115">Description</span><span class="sxs-lookup"><span data-stu-id="354ab-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="354ab-116">**\_nom m**</span><span class="sxs-lookup"><span data-stu-id="354ab-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="354ab-117">Nom du filtre.</span><span class="sxs-lookup"><span data-stu-id="354ab-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="354ab-118">**m \_ ClsID**</span><span class="sxs-lookup"><span data-stu-id="354ab-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="354ab-119">Pointeur vers le CLSID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="354ab-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="354ab-120">**m \_ lpfnNew**</span><span class="sxs-lookup"><span data-stu-id="354ab-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="354ab-121">Pointeur vers une fonction qui crée une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="354ab-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="354ab-122">**m \_ lpfnInit**</span><span class="sxs-lookup"><span data-stu-id="354ab-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="354ab-123">Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.</span><span class="sxs-lookup"><span data-stu-id="354ab-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="354ab-124">**\_filtre m pAMovieSetup \_**</span><span class="sxs-lookup"><span data-stu-id="354ab-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="354ab-125">Pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="354ab-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="354ab-126">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="354ab-126">Public Methods</span></span>                                                            | <span data-ttu-id="354ab-127">Description</span><span class="sxs-lookup"><span data-stu-id="354ab-127">Description</span></span>                                                                |
| [<span data-ttu-id="354ab-128">**IsClassID**</span><span class="sxs-lookup"><span data-stu-id="354ab-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="354ab-129">Détermine si un CLSID correspond à ce modèle de classe.</span><span class="sxs-lookup"><span data-stu-id="354ab-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="354ab-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="354ab-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="354ab-131">Appelle la fonction de création d’objet pour la classe.</span><span class="sxs-lookup"><span data-stu-id="354ab-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="354ab-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="354ab-132">Requirements</span></span>



| <span data-ttu-id="354ab-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="354ab-133">Requirement</span></span> | <span data-ttu-id="354ab-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="354ab-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354ab-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="354ab-135">Header</span></span><br/>  | <dl> <span data-ttu-id="354ab-136"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="354ab-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="354ab-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="354ab-137">Library</span></span><br/> | <dl> <span data-ttu-id="354ab-138"><dt>Strmbase. lib ; </dt> <dt>Strmbasd. lib</dt></span><span class="sxs-lookup"><span data-stu-id="354ab-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="354ab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="354ab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354ab-140">Référence de classe de base</span><span class="sxs-lookup"><span data-stu-id="354ab-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

