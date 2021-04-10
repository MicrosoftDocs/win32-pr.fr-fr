---
title: ILockBytes-implémentation de la mémoire globale
description: L’implémentation de la mémoire globale ILockBytes est implémentée sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçue pour lire et écrire directement dans la mémoire globale.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implémentations, mémoire globale
- ILockBytes Strctd STG, implémentations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309473"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="af58f-105">ILockBytes-implémentation de la mémoire globale</span><span class="sxs-lookup"><span data-stu-id="af58f-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="af58f-106">L’implémentation de la mémoire globale ILockBytes est implémentée sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçue pour lire et écrire directement dans la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="af58f-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="af58f-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="af58f-107">When to Use</span></span>

<span data-ttu-id="af58f-108">Les méthodes de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont appelées à partir des implémentations de fichiers composés de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sur l’objet de stockage de fichiers composés créé via un appel à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span><span class="sxs-lookup"><span data-stu-id="af58f-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="af58f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="af58f-109">Remarks</span></span>

<span data-ttu-id="af58f-110">Voici les méthodes de l’implémentation de la mémoire globale [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="af58f-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="af58f-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes :: readatum**</span><span class="sxs-lookup"><span data-stu-id="af58f-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-112">Lit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="af58f-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes :: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="af58f-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-114">Écrit le bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="af58f-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes :: Flush**</span><span class="sxs-lookup"><span data-stu-id="af58f-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-116">Contrairement à l’implémentation basée sur les fichiers, l’appel de cette méthode dans l’implémentation de la mémoire globale n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="af58f-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes :: configure**</span><span class="sxs-lookup"><span data-stu-id="af58f-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-118">Définit la taille du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="af58f-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes :: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="af58f-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-120">Cette implémentation ne prend pas en charge le verrouillage, donc *dwLocksType* a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="af58f-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="af58f-121">L’appelant doit s’assurer que les accès sont valides et s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="af58f-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes :: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="af58f-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-123">Cette implémentation ne prend pas en charge le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="af58f-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="af58f-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes :: stat**</span><span class="sxs-lookup"><span data-stu-id="af58f-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="af58f-125">L’implémentation [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fournie par com appelle la méthode [**ILockBytes :: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) pour récupérer des données sur l’objet de tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="af58f-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="af58f-126">S’il n’existe pas de nom raisonnable pour le tableau d’octets, la méthode **ILockBytes :: stat** fournie par com retourne **null** dans le membre **pwcsName** de la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="af58f-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="af58f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af58f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af58f-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="af58f-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="af58f-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="af58f-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="af58f-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="af58f-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




