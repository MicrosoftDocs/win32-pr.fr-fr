---
title: Implémentation de File-Based ILockBytes
description: Implémenté sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçu pour lire et écrire directement dans un fichier sur disque.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implémentations, basé sur des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379689"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="c7f09-104">Implémentation de File-Based ILockBytes</span><span class="sxs-lookup"><span data-stu-id="c7f09-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="c7f09-105">Implémenté sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçu pour lire et écrire directement dans un fichier sur disque.</span><span class="sxs-lookup"><span data-stu-id="c7f09-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c7f09-106">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c7f09-106">When to Use</span></span>

<span data-ttu-id="c7f09-107">Les méthodes de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont appelées à partir des implémentations de fichiers composés de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sur l’objet de stockage de fichiers composés créé via un appel à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile). vous n’avez donc pas besoin de les appeler directement.</span><span class="sxs-lookup"><span data-stu-id="c7f09-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f09-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c7f09-108">Remarks</span></span>

<span data-ttu-id="c7f09-109">Voici les méthodes de l’implémentation de File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="c7f09-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="c7f09-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes :: readatum**</span><span class="sxs-lookup"><span data-stu-id="c7f09-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-111">Lit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c7f09-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes :: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="c7f09-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-113">Écrit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c7f09-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes :: Flush**</span><span class="sxs-lookup"><span data-stu-id="c7f09-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-115">Garantit que toutes les mémoires tampons internes gérées par l’implémentation [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont écrites dans le stockage physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c7f09-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes :: configure**</span><span class="sxs-lookup"><span data-stu-id="c7f09-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-117">Définit la taille du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c7f09-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes :: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="c7f09-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-119">Le paramètre *dwLockTypes* est défini sur lock \_ ONLYONCE ou Lock \_ exclusive, ce qui autorise ou limite l’accès aux régions verrouillées.</span><span class="sxs-lookup"><span data-stu-id="c7f09-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes :: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="c7f09-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-121">Cette méthode déverrouille la région verrouillée par [**ILockBytes :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span><span class="sxs-lookup"><span data-stu-id="c7f09-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="c7f09-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes :: stat**</span><span class="sxs-lookup"><span data-stu-id="c7f09-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="c7f09-123">L’implémentation [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fournie par com appelle la méthode [**ILockBytes :: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) pour récupérer les informations sur l’objet de tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c7f09-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="c7f09-124">S’il n’existe pas de nom raisonnable pour le tableau d’octets, la méthode **ILockBytes :: stat** fournie par com retourne **null** dans le membre **pwcsName** de la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="c7f09-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c7f09-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7f09-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7f09-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c7f09-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="c7f09-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="c7f09-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="c7f09-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="c7f09-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




