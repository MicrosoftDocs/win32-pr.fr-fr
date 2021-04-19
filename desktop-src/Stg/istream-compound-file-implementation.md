---
title: IStream-implémentation de fichier composé
description: L’interface IStream prend en charge la lecture et l’écriture de données dans des objets de flux. Dans un objet de stockage structuré, les objets de flux contiennent les données et les stockages fournissent la structure.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106529514"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="a3d49-105">IStream-implémentation de fichier composé</span><span class="sxs-lookup"><span data-stu-id="a3d49-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="a3d49-106">L’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) prend en charge la lecture et l’écriture de données dans des objets de flux.</span><span class="sxs-lookup"><span data-stu-id="a3d49-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="a3d49-107">Dans un objet de stockage structuré, les objets de flux contiennent les données et les stockages fournissent la structure.</span><span class="sxs-lookup"><span data-stu-id="a3d49-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="a3d49-108">Les données simples peuvent être écrites directement dans un flux, mais plus fréquemment, les flux sont des éléments imbriqués dans un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="a3d49-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="a3d49-109">Elles sont similaires aux fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="a3d49-109">They are similar to standard files.</span></span>

<span data-ttu-id="a3d49-110">La spécification de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) définit davantage de fonctionnalités que celles prises en charge par l’implémentation com.</span><span class="sxs-lookup"><span data-stu-id="a3d49-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="a3d49-111">Par exemple, l’interface **IStream** définit des flux d’une longueur maximale de 2 ⁶ ⁴ octets nécessitant un pointeur de recherche de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a3d49-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="a3d49-112">Toutefois, l’implémentation COM prend uniquement en charge les flux allant jusqu’à 2 ³ octets ² en longueur (4 Go) et les opérations de lecture et d’écriture sont toujours limitées à 2 ³ ² octets à la fois.</span><span class="sxs-lookup"><span data-stu-id="a3d49-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="a3d49-113">L’implémentation COM ne prend pas non plus en charge les transactions de flux ou le verrouillage de région.</span><span class="sxs-lookup"><span data-stu-id="a3d49-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="a3d49-114">Pour créer un flux simple basé sur la mémoire globale, récupérez un pointeur [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en appelant la fonction d’API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span><span class="sxs-lookup"><span data-stu-id="a3d49-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="a3d49-115">Pour obtenir un pointeur **IStream** dans un objet de fichier composé, appelez [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span><span class="sxs-lookup"><span data-stu-id="a3d49-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="a3d49-116">Ces fonctions récupèrent un pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , avec lequel vous pouvez ensuite appeler [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) pour un pointeur **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a3d49-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="a3d49-117">Dans les deux cas, le même code d’implémentation **IStream** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a3d49-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="a3d49-118">L’implémentation de fichier composé de stockage structuré ne fonctionne pas sur une méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), mais elle comprend les méthodes [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) et [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) via le pointeur d’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="a3d49-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="a3d49-119">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a3d49-119">When to Use</span></span>

<span data-ttu-id="a3d49-120">Appeler les méthodes de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pour lire et écrire des données dans un flux.</span><span class="sxs-lookup"><span data-stu-id="a3d49-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="a3d49-121">Étant donné que les objets de flux peuvent être marshalés vers d’autres processus, les applications peuvent partager les données dans des objets de stockage sans avoir à utiliser de la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="a3d49-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="a3d49-122">Dans l’implémentation de fichier composé COM des objets de flux, les fonctions de marshaling personnalisées dans COM créent une version distante de l’objet d’origine dans le nouveau processus lorsque les deux processus ont accès à la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="a3d49-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="a3d49-123">Par conséquent, la version distante n’a pas besoin de communiquer avec le processus d’origine pour exécuter ses fonctions.</span><span class="sxs-lookup"><span data-stu-id="a3d49-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="a3d49-124">La version distante de l’objet de flux partage le même pointeur de recherche que le flux d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3d49-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="a3d49-125">Si vous ne souhaitez pas partager le pointeur de recherche, utilisez la méthode [**IStream :: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) pour fournir une copie de l’objet de flux pour le processus distant.</span><span class="sxs-lookup"><span data-stu-id="a3d49-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="a3d49-126">Si vous créez un objet de flux plus grand que le tas dans la mémoire de votre ordinateur et que vous utilisez un descripteur **HGLOBAL** à un objet de mémoire global, l’objet de flux appelle la méthode [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) en interne whe il requiert plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a3d49-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="a3d49-127">Étant donné que **GlobalReAlloc** copie toujours les données de la source vers la destination, le fait d’augmenter un objet de flux de 20 Mo à 25 Mo, par exemple, nécessite un temps considérable.</span><span class="sxs-lookup"><span data-stu-id="a3d49-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="a3d49-128">Cela est dû à la taille des incréments copiés et est aggravé s’il y a moins de 45 Mo de mémoire sur l’ordinateur en raison de l’échange de disque.</span><span class="sxs-lookup"><span data-stu-id="a3d49-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="a3d49-129">La solution recommandée consiste à implémenter une méthode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) qui utilise la mémoire allouée par [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) au lieu de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="a3d49-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="a3d49-130">Cela peut réserver un grand segment d’espace d’adressage virtuel, puis valider la mémoire dans cet espace d’adressage en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="a3d49-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="a3d49-131">Aucune copie de données ne se produit et la mémoire n’est validée que si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a3d49-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="a3d49-132">Une alternative à [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) consiste à appeler la méthode [**IStream :: desets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) sur l’objet de flux pour augmenter l’allocation de mémoire à l’avance.</span><span class="sxs-lookup"><span data-stu-id="a3d49-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="a3d49-133">Toutefois, ce n’est pas aussi efficace que l’utilisation de [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a3d49-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="a3d49-134">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3d49-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="a3d49-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream :: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="a3d49-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-136">Lit un nombre spécifié d'octets à partir de l'objet de flux dans la mémoire en commençant au niveau du pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="a3d49-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="a3d49-137">Cette implémentation retourne S \_ OK si la fin du flux a été atteinte pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="a3d49-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="a3d49-138">(Il s’agit du même comportement que celui de la « fin du fichier » trouvé dans le système de fichiers FAT MS-DOS.)</span><span class="sxs-lookup"><span data-stu-id="a3d49-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream :: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="a3d49-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-140">Écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="a3d49-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="a3d49-141">Dans cette implémentation, les objets de flux ne sont pas éparpillés.</span><span class="sxs-lookup"><span data-stu-id="a3d49-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="a3d49-142">Tout octet de remplissage est finalement alloué sur le disque et affecté au flux.</span><span class="sxs-lookup"><span data-stu-id="a3d49-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream :: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="a3d49-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-144">Modifie le pointeur de recherche vers un nouvel emplacement relatif au début du flux, à la fin du flux, ou au pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="a3d49-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream :: assets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="a3d49-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-146">Modifie la taille de l'objet de flux.</span><span class="sxs-lookup"><span data-stu-id="a3d49-146">Changes the size of the stream object.</span></span> <span data-ttu-id="a3d49-147">Dans cette implémentation, il n’y a aucune garantie que l’espace alloué sera contigu.</span><span class="sxs-lookup"><span data-stu-id="a3d49-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="a3d49-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-149">Copie un nombre spécifié d'octets à partir du pointeur de recherche actuel d'un flux vers le pointeur de recherche actuel d'un autre flux.</span><span class="sxs-lookup"><span data-stu-id="a3d49-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="a3d49-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-151">L’implémentation de fichier composé de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) prend en charge l’ouverture des flux uniquement en mode direct, et non en mode traité.</span><span class="sxs-lookup"><span data-stu-id="a3d49-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="a3d49-152">Par conséquent, la méthode n’a aucun effet quand elle est appelée, sauf pour vider toutes les mémoires tampons de mémoire au niveau de stockage suivant.</span><span class="sxs-lookup"><span data-stu-id="a3d49-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="a3d49-153">Dans cette implémentation, peu importe si vous validez des modifications apportées aux flux, vous n’avez besoin que de valider les modifications des objets de stockage.</span><span class="sxs-lookup"><span data-stu-id="a3d49-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream :: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="a3d49-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-155">Cette implémentation ne prend pas en charge les flux transactionnels, donc un appel à cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="a3d49-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="a3d49-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-157">Le verrouillage de plage n’est pas pris en charge par cette implémentation, donc un appel à cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="a3d49-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream :: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="a3d49-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-159">Supprime la restriction d’accès sur une plage d’octets précédemment restreinte avec [**IStream :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span><span class="sxs-lookup"><span data-stu-id="a3d49-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="a3d49-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-161">Récupère la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) pour ce flux</span><span class="sxs-lookup"><span data-stu-id="a3d49-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="a3d49-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream :: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="a3d49-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="a3d49-163">Crée un objet de flux avec son propre pointeur de recherche qui référence les mêmes octets que le flux d'origine.</span><span class="sxs-lookup"><span data-stu-id="a3d49-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="a3d49-164">Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en mode simple est soumis aux contraintes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3d49-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="a3d49-165">Un flux est en mode simple s’il a été créé ou ouvert à partir d’un stockage en mode simple.</span><span class="sxs-lookup"><span data-stu-id="a3d49-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="a3d49-166">Un stockage est un mode simple s’il est créé ou ouvert avec l' \_ indicateur simple STGM défini dans le paramètre *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="a3d49-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="a3d49-167">Les méthodes [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) et [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a3d49-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="a3d49-168">La méthode [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) est prise en charge, mais la \_ valeur NoName StatFlag doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a3d49-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3d49-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3d49-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3d49-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="a3d49-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="a3d49-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="a3d49-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="a3d49-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="a3d49-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="a3d49-173">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="a3d49-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="a3d49-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="a3d49-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 