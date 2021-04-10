---
title: Implémentation de fichiers IEnumSTATPROPSTG-Compound
description: L’implémentation de fichier composé de l’interface IEnumSTATPROPSTG est utilisée pour énumérer des propriétés, ce qui donne des structures STATPROPSTG, qui contiennent des données de propriété statistiques.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941265"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="85906-104">Implémentation de fichiers IEnumSTATPROPSTG-Compound</span><span class="sxs-lookup"><span data-stu-id="85906-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="85906-105">L’implémentation de fichier composé de l’interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) est utilisée pour énumérer des propriétés, ce qui donne des structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , qui contiennent des données de propriété statistiques.</span><span class="sxs-lookup"><span data-stu-id="85906-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="85906-106">L’implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gère les données statistiques et est associée à un objet de stockage de fichiers composés actuel.</span><span class="sxs-lookup"><span data-stu-id="85906-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="85906-107">Le constructeur de l’implémentation COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crée une classe qui lit le jeu de propriétés entier et crée un tableau statique qui peut être partagé lorsque **IEnumSTATPROPSTG :: Clone** est appelé.</span><span class="sxs-lookup"><span data-stu-id="85906-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="85906-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="85906-108">When to Use</span></span>

<span data-ttu-id="85906-109">Appelez l’implémentation de fichier composé de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) qui contiennent des données sur les propriétés dans le jeu de propriétés actuel.</span><span class="sxs-lookup"><span data-stu-id="85906-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="85906-110">Quand vous utilisez l’implémentation de fichier composé des interfaces de stockage des propriétés, appelez [**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) pour retourner un pointeur vers **IEnumSTATPROPSTG** pour gérer l’objet de stockage de propriétés et les éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="85906-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="85906-111">Notes</span><span class="sxs-lookup"><span data-stu-id="85906-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="85906-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG :: suivant**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="85906-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="85906-113">Obtient le suivant d’une ou plusieurs structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (le nombre est spécifié par le paramètre *celt* ).</span><span class="sxs-lookup"><span data-stu-id="85906-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="85906-114">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="85906-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="85906-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG :: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="85906-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="85906-116">Ignore le nombre d’éléments spécifiés dans *celt*.</span><span class="sxs-lookup"><span data-stu-id="85906-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="85906-117">L’élément suivant à énumérer par le biais d’un appel à Next devient alors l’élément après les éléments ignorés.</span><span class="sxs-lookup"><span data-stu-id="85906-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="85906-118">Retourne S \_ OK si les éléments *celt* ont été ignorés ; retourne la \_ valeur false si moins de *celt* Elements ont été ignorés.</span><span class="sxs-lookup"><span data-stu-id="85906-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="85906-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG :: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="85906-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="85906-120">Définit le curseur au début de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="85906-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="85906-121">En cas de réussite, retourne S \_ OK ; sinon, retourne STG \_ E \_ INVALIDHANDLE.</span><span class="sxs-lookup"><span data-stu-id="85906-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="85906-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG :: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="85906-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="85906-123">Utilise le constructeur pour le [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) pour créer une copie du tableau.</span><span class="sxs-lookup"><span data-stu-id="85906-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="85906-124">Étant donné que la classe qui construit le tableau statique contient en fait l’objet, cette fonction ajoute principalement au décompte de références.</span><span class="sxs-lookup"><span data-stu-id="85906-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="85906-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85906-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85906-126">**STATPROPSTG**</span><span class="sxs-lookup"><span data-stu-id="85906-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="85906-127">**IPropertyStorage :: enum**</span><span class="sxs-lookup"><span data-stu-id="85906-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 