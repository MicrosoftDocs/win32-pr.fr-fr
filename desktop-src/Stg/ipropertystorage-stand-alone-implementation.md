---
title: IPropertyStorage-implémentation autonome
description: L’implémentation autonome fournie par le système de IPropertySetStorage comprend une implémentation de IPropertyStorage, l’interface qui lit et écrit des propriétés dans un stockage de jeu de propriétés.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-implémentation autonome
- IPropertyStorage Strctd STG, implémentations, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382125"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="18f36-105">IPropertyStorage-implémentation autonome</span><span class="sxs-lookup"><span data-stu-id="18f36-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="18f36-106">L’implémentation autonome fournie par le système de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) comprend une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l’interface qui lit et écrit des propriétés dans un stockage de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="18f36-107">L’interface **IPropertySetStorage** crée et ouvre les jeux de propriétés dans un stockage.</span><span class="sxs-lookup"><span data-stu-id="18f36-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="18f36-108">Les interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) et [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sont également fournies dans l’implémentation autonome.</span><span class="sxs-lookup"><span data-stu-id="18f36-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="18f36-109">Pour obtenir un pointeur vers l’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), appelez la fonction [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) pour créer un nouveau jeu de propriétés ou [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) pour obtenir le pointeur d’interface sur un jeu de propriétés existant (ou appelez les méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de l’implémentation autonome [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).</span><span class="sxs-lookup"><span data-stu-id="18f36-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="18f36-110">L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crée des jeux de propriétés sur n’importe quel objet de stockage ou de flux, pas seulement sur des flux et des stockages de fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="18f36-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="18f36-111">L’implémentation autonome ne dépend pas de fichiers composés et peut être utilisée avec n’importe quelle implémentation de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="18f36-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="18f36-112">Pour plus d’informations sur l’implémentation de fichier composé de cette interface, consultez [implémentation de fichiers composés IPropertyStorage](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="18f36-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="18f36-113">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="18f36-113">When to Use</span></span>

<span data-ttu-id="18f36-114">Utilisez [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pour gérer les propriétés dans un même jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="18f36-115">Ses méthodes prennent en charge la lecture, l’écriture et la suppression des propriétés et des noms de chaînes facultatifs qui peuvent être associés à des ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="18f36-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="18f36-116">Les autres méthodes prennent en charge la validation standard et les opérations de restauration de stockage.</span><span class="sxs-lookup"><span data-stu-id="18f36-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="18f36-117">Il existe également une méthode qui définit les heures associées au stockage des propriétés, et une autre qui permet l’affectation d’un CLSID à utiliser pour associer un autre code, tel que le code de l’interface utilisateur, au jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="18f36-118">La méthode [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fournit un pointeur vers l’implémentation autonome de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), qui énumère les propriétés du jeu.</span><span class="sxs-lookup"><span data-stu-id="18f36-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="18f36-119">Formats de jeu de propriétés de la version 0 et de la version 1</span><span class="sxs-lookup"><span data-stu-id="18f36-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="18f36-120">L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les formats de sérialisation des jeux de propriétés version 0 et version 1.</span><span class="sxs-lookup"><span data-stu-id="18f36-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="18f36-121">Pour plus d’informations, consultez [sérialisation du jeu de propriétés](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="18f36-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="18f36-122">Les jeux de propriétés sont créés au format version 0 et restent dans ce format, sauf si de nouvelles fonctionnalités sont demandées.</span><span class="sxs-lookup"><span data-stu-id="18f36-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="18f36-123">À ce moment-là, le format est mis à jour vers la version 1.</span><span class="sxs-lookup"><span data-stu-id="18f36-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="18f36-124">Par exemple, si un jeu de propriétés est créé avec l' \_ indicateur par défaut PROPSETFLAG, son format est version 0.</span><span class="sxs-lookup"><span data-stu-id="18f36-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="18f36-125">Tant que les types de propriété conformes au format de version 0 sont écrits et lus à partir de ce jeu de propriétés, le jeu de propriétés reste au format de la version 0.</span><span class="sxs-lookup"><span data-stu-id="18f36-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="18f36-126">Si un type de propriété de la version 1 est écrit dans le jeu de propriétés, le jeu de propriétés est automatiquement mis à jour vers la version 1.</span><span class="sxs-lookup"><span data-stu-id="18f36-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="18f36-127">Par la suite, ce jeu de propriétés ne peut plus être lu par les implémentations qui comprennent uniquement la version 0.</span><span class="sxs-lookup"><span data-stu-id="18f36-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="18f36-128">Types IPropertyStorage et variant</span><span class="sxs-lookup"><span data-stu-id="18f36-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="18f36-129">L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ne prend pas en charge les types variant VT \_ Unknown ou VT \_ Dispatch dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="18f36-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="18f36-130">Les types variant suivants sont pris en charge dans un SafeArray ; autrement dit, ces valeurs peuvent être combinées avec \_ un tableau VT dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="18f36-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="18f36-131">Types variant pris en charge dans SafeArray par implémentation de fichier composé de [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="18f36-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="18f36-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="18f36-132">VT\_I1</span></span>

<span data-ttu-id="18f36-133">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="18f36-133">VT\_UI1</span></span>

<span data-ttu-id="18f36-134">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="18f36-134">VT\_I2</span></span>

<span data-ttu-id="18f36-135">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="18f36-135">VT\_UI2</span></span>

<span data-ttu-id="18f36-136">VT \_</span><span class="sxs-lookup"><span data-stu-id="18f36-136">VT\_I4</span></span>

<span data-ttu-id="18f36-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="18f36-137">VT\_UI4</span></span>

<span data-ttu-id="18f36-138">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="18f36-138">VT\_INT</span></span>

<span data-ttu-id="18f36-139">VT \_ uint</span><span class="sxs-lookup"><span data-stu-id="18f36-139">VT\_UINT</span></span>

<span data-ttu-id="18f36-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="18f36-140">VT\_R4</span></span>

<span data-ttu-id="18f36-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="18f36-141">VT\_R8</span></span>

<span data-ttu-id="18f36-142">VT \_ ca</span><span class="sxs-lookup"><span data-stu-id="18f36-142">VT\_CY</span></span>

<span data-ttu-id="18f36-143">\_Date VT</span><span class="sxs-lookup"><span data-stu-id="18f36-143">VT\_DATE</span></span>

<span data-ttu-id="18f36-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="18f36-144">VT\_BSTR</span></span>

<span data-ttu-id="18f36-145">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="18f36-145">VT\_BOOL</span></span>

<span data-ttu-id="18f36-146">\_valeur décimale VT</span><span class="sxs-lookup"><span data-stu-id="18f36-146">VT\_DECIMAL</span></span>

<span data-ttu-id="18f36-147">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="18f36-147">VT\_ERROR</span></span>

<span data-ttu-id="18f36-148">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="18f36-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="18f36-149">Lorsque VT \_ Variant est combiné avec \_ un tableau VT, le SAFEARRAY lui-même contient des structures [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="18f36-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="18f36-150">Toutefois, les types de ces éléments doivent être extraits de la liste précédente, ne peuvent pas être des \_ variantes VT et ne peuvent pas inclure les \_ indicateurs de vecteur VT, de \_ matrice VT ou VT \_ .</span><span class="sxs-lookup"><span data-stu-id="18f36-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="18f36-151">Méthodes IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="18f36-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="18f36-152">L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="18f36-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="18f36-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="18f36-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-154">Lit les propriétés spécifiées dans le tableau *rgpspec* et fournit les valeurs de toutes les propriétés valides dans le tableau *rgvar* d’éléments [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="18f36-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="18f36-155">Dans l’implémentation fournie par le système, les identificateurs de propriété dupliqués qui font référence aux types de flux ou de stockage entraînent plusieurs appels à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) et la réussite ou l’échec de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) dépend de la capacité de l’implémentation de stockage sous-jacente à partager les stockages ouverts.</span><span class="sxs-lookup"><span data-stu-id="18f36-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="18f36-156">En outre, pour garantir une opération thread-safe si la même propriété de flux ou de valeur de stockage est demandée plusieurs fois via le même pointeur [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , l’ouverture réussira ou échouera selon que la propriété est déjà ouverte et que le système de fichiers sous-jacent gère plusieurs ouvertures d’un flux ou d’un stockage.</span><span class="sxs-lookup"><span data-stu-id="18f36-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="18f36-157">Ainsi, l’opération [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) sur une propriété de flux ou de valeur de stockage entraîne toujours un appel à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), en passant l’accès (STGM \_ ReadWrite, par exemple) et les valeurs de partage (STGM \_ partage \_ exclusive, par exemple) spécifié lors de l’ouverture ou de la création initiale du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="18f36-158">Si la méthode échoue, les valeurs écrites dans *rgvar* \[ \] ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="18f36-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="18f36-159">Si certaines propriétés de flux ou de valeur de stockage sont ouvertes avec succès mais qu’une erreur se produit avant la fin de l’exécution, ces propriétés doivent être libérées avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="18f36-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="18f36-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-161">Écrit les propriétés spécifiées dans le tableau *rgpspec* , en leur \[ \] assignant les balises et les valeurs [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) spécifiées dans *rgvar* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="18f36-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="18f36-162">Les valeurs **PROPVARIANT** spécifiées sont affectées aux propriétés qui existent déjà, et les propriétés qui n’existent pas actuellement sont créées.</span><span class="sxs-lookup"><span data-stu-id="18f36-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage ::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="18f36-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-164">Supprime les propriétés spécifiées dans *rgpspec* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="18f36-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="18f36-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="18f36-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-166">Lit les noms de chaîne existants associés aux ID de propriété spécifiés dans le tableau *rgpropid* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="18f36-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="18f36-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-168">Attribue des noms de chaîne spécifiés dans le tableau *rglpwstrName* aux ID de propriété spécifiés dans le tableau *rgpropid* .</span><span class="sxs-lookup"><span data-stu-id="18f36-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage ::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="18f36-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-170">Supprime les noms de chaîne des ID de propriété spécifiés dans le tableau *rgpropid* en écrivant la **valeur null** dans le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="18f36-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="18f36-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-172">Définit le **CLSID** du flux de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="18f36-173">Dans l’implémentation autonome, la définition du CLSID sur un jeu de propriétés non simple (un qui peut contenir des propriétés de stockage ou de valeur de flux, comme décrit dans [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) définit également le CLSID sur le sous-stockage sous-jacent afin qu’il puisse être obtenu via un appel à [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span><span class="sxs-lookup"><span data-stu-id="18f36-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="18f36-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="18f36-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-175">Pour les jeux de propriétés simples et simples, vide l’image mémoire sur le sous-système de disque.</span><span class="sxs-lookup"><span data-stu-id="18f36-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="18f36-176">En outre, pour les jeux de propriétés de mode transactionnel non simple, cette méthode appelle [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sur le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="18f36-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage :: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="18f36-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-178">Pour les jeux de propriétés qui ne sont pas simples, appelle la méthode [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) du stockage sous-jacent et ouvre à nouveau le flux de contenu.</span><span class="sxs-lookup"><span data-stu-id="18f36-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="18f36-179">Pour les jeux de propriétés simples, retourne uniquement E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18f36-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="18f36-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-181">Crée un objet énumérateur qui implémente [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), dont les méthodes peuvent être appelées pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) qui fournissent des informations sur chacune des propriétés de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="18f36-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="18f36-182">Cette implémentation crée un tableau dans lequel le jeu de propriétés entier est lu et qui peut être partagé quand [**IEnumSTATPROPSTG :: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) est appelé.</span><span class="sxs-lookup"><span data-stu-id="18f36-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage :: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="18f36-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-184">Remplit les membres d’une structure [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , qui contient des informations sur la propriété définie dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="18f36-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="18f36-185">Au retour, fournit un pointeur vers la structure.</span><span class="sxs-lookup"><span data-stu-id="18f36-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="18f36-186">Pour les jeux de stockage qui ne sont pas simples, cette implémentation appelle [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) pour obtenir les informations à partir du flux ou du stockage sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="18f36-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="18f36-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="18f36-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="18f36-188">Pour les jeux de propriétés qui ne sont pas simples, définit les heures prises en charge par le stockage sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="18f36-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="18f36-189">Cette implémentation de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) appelle la méthode [**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) du stockage sous-jacent pour modifier les heures.</span><span class="sxs-lookup"><span data-stu-id="18f36-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="18f36-190">Il prend en charge les heures prises en charge par la méthode sous-jacente, qui peuvent être l’heure de modification, le temps d’accès ou l’heure de création.</span><span class="sxs-lookup"><span data-stu-id="18f36-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="18f36-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18f36-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18f36-192">IPropertySetStorage-implémentation autonome</span><span class="sxs-lookup"><span data-stu-id="18f36-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="18f36-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="18f36-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="18f36-194">**IStorage :: SetElementTimes**</span><span class="sxs-lookup"><span data-stu-id="18f36-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="18f36-195">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="18f36-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="18f36-196">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="18f36-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="18f36-197">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="18f36-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 