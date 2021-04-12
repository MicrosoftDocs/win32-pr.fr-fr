---
title: Constantes STGM (ObjBase. h)
description: Indicateurs qui indiquent des conditions pour la création et la suppression des objets et des modes d’accès pour l’objet.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464483"
---
# <a name="stgm-constants"></a><span data-ttu-id="4aad1-103">Constantes STGM</span><span class="sxs-lookup"><span data-stu-id="4aad1-103">STGM Constants</span></span>

<span data-ttu-id="4aad1-104">Les constantes STGM sont des indicateurs qui indiquent des conditions pour la création et la suppression des modes d’accès et d’objet pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="4aad1-105">Les constantes STGM sont incluses dans les interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et dans les fonctions [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)et [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="4aad1-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="4aad1-106">Ces éléments sont souvent combinés à l’aide d’un opérateur **or**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="4aad1-107">Elles sont interprétées dans des groupes répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4aad1-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="4aad1-108">L’utilisation de plusieurs éléments à partir d’un seul groupe n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4aad1-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="4aad1-109">Utilisez un indicateur du groupe de création lors de la création d’un objet, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="4aad1-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="4aad1-110">Pour plus d’informations sur les transactions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="4aad1-111">Group</span><span class="sxs-lookup"><span data-stu-id="4aad1-111">Group</span></span>                      | <span data-ttu-id="4aad1-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="4aad1-112">Flag</span></span>                         | <span data-ttu-id="4aad1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aad1-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="4aad1-114">Accès</span><span class="sxs-lookup"><span data-stu-id="4aad1-114">Access</span></span>                     | <span data-ttu-id="4aad1-115">**\_lecture STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-115">**STGM\_READ**</span></span>               | <span data-ttu-id="4aad1-116">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="4aad1-117">**\_écriture STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="4aad1-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="4aad1-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="4aad1-119">**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="4aad1-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="4aad1-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="4aad1-120">0x00000002L</span></span> |
| <span data-ttu-id="4aad1-121">Partage</span><span class="sxs-lookup"><span data-stu-id="4aad1-121">Sharing</span></span>                    | <span data-ttu-id="4aad1-122">**\_partage STGM \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="4aad1-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="4aad1-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="4aad1-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="4aad1-124">**\_ \_ lecture refusée du partage STGM \_**</span><span class="sxs-lookup"><span data-stu-id="4aad1-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="4aad1-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="4aad1-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="4aad1-126">**\_partage STGM \_ refuser l' \_ écriture**</span><span class="sxs-lookup"><span data-stu-id="4aad1-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="4aad1-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="4aad1-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="4aad1-128">**\_partage STGM \_ exclusif**</span><span class="sxs-lookup"><span data-stu-id="4aad1-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="4aad1-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="4aad1-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="4aad1-130">**\_priorité STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="4aad1-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-131">0x00040000L</span></span> |
| <span data-ttu-id="4aad1-132">Création</span><span class="sxs-lookup"><span data-stu-id="4aad1-132">Creation</span></span>                   | <span data-ttu-id="4aad1-133">**STGM \_ créer**</span><span class="sxs-lookup"><span data-stu-id="4aad1-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="4aad1-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="4aad1-135">**STGM \_ convertir**</span><span class="sxs-lookup"><span data-stu-id="4aad1-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="4aad1-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="4aad1-137">**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="4aad1-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="4aad1-138">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-138">0x00000000L</span></span> |
| <span data-ttu-id="4aad1-139">Transactions</span><span class="sxs-lookup"><span data-stu-id="4aad1-139">Transactioning</span></span>             | <span data-ttu-id="4aad1-140">**STGM \_ direct**</span><span class="sxs-lookup"><span data-stu-id="4aad1-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="4aad1-141">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="4aad1-142">**STGM \_ traité**</span><span class="sxs-lookup"><span data-stu-id="4aad1-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="4aad1-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-143">0x00010000L</span></span> |
| <span data-ttu-id="4aad1-144">Performances des transactions</span><span class="sxs-lookup"><span data-stu-id="4aad1-144">Transactioning Performance</span></span> | <span data-ttu-id="4aad1-145">**STGM \_ NOrayer**</span><span class="sxs-lookup"><span data-stu-id="4aad1-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="4aad1-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="4aad1-147">**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="4aad1-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="4aad1-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-148">0x00200000L</span></span> |
| <span data-ttu-id="4aad1-149">SWMR directe et simple</span><span class="sxs-lookup"><span data-stu-id="4aad1-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="4aad1-150">**STGM \_ simple**</span><span class="sxs-lookup"><span data-stu-id="4aad1-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="4aad1-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="4aad1-152">**STGM \_ direct \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="4aad1-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="4aad1-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-153">0x00400000L</span></span> |
| <span data-ttu-id="4aad1-154">Supprimer au lancement</span><span class="sxs-lookup"><span data-stu-id="4aad1-154">Delete On Release</span></span>          | <span data-ttu-id="4aad1-155">**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="4aad1-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="4aad1-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="4aad1-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**\_lecture STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-158">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-159">Indique que l’objet est en lecture seule, ce qui signifie que les modifications ne peuvent pas être effectuées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="4aad1-160">Par exemple, si un objet de flux est ouvert avec **STGM \_ Read**, la méthode [**ISequentialStream :: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) peut être appelée, mais la méthode [**ISequentialStream :: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) peut ne pas l’être.</span><span class="sxs-lookup"><span data-stu-id="4aad1-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="4aad1-161">De même, si un objet de stockage ouvert avec **STGM est \_ lu**, les méthodes [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) et [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) peuvent être appelées, mais les méthodes [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) et [**IStorage :: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) peuvent ne pas l’être.</span><span class="sxs-lookup"><span data-stu-id="4aad1-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**\_écriture STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="4aad1-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-164">Vous permet d’enregistrer les modifications apportées à l’objet, mais n’autorise pas l’accès à ses données.</span><span class="sxs-lookup"><span data-stu-id="4aad1-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="4aad1-165">Les implémentations fournies des interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ne prennent pas en charge ce mode en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="4aad1-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="4aad1-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="4aad1-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-168">Active l’accès et la modification des données d’objet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-168">Enables access and modification of object data.</span></span> <span data-ttu-id="4aad1-169">Par exemple, si un objet de flux est créé ou ouvert dans ce mode, il est possible d’appeler à la fois [**IStream :: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) et **IStream :: Write**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="4aad1-170">N’oubliez pas que cette constante n’est pas un simple fichier binaire **ou** une opération des éléments de **\_ lecture** **STGM \_ Write** et STGM.</span><span class="sxs-lookup"><span data-stu-id="4aad1-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**\_partage STGM \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="4aad1-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="4aad1-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-173">Spécifie que l’accès en lecture ou en écriture n’est pas refusé aux ouvertures suivantes de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="4aad1-174">Si aucun indicateur du groupe de partage n’est spécifié, cet indicateur est supposé.</span><span class="sxs-lookup"><span data-stu-id="4aad1-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**\_ \_ lecture refusée du partage STGM \_**</span><span class="sxs-lookup"><span data-stu-id="4aad1-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="4aad1-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-177">Empêche d’autres utilisateurs d’ouvrir l’objet en mode de **\_ lecture STGM** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="4aad1-178">Il est généralement utilisé sur un objet de stockage racine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**\_partage STGM \_ refuser l' \_ écriture**</span><span class="sxs-lookup"><span data-stu-id="4aad1-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="4aad1-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-181">Empêche d’autres utilisateurs d’ouvrir l’objet pour **STGM \_ Write** ou **STGM \_ ReadWrite** Access.</span><span class="sxs-lookup"><span data-stu-id="4aad1-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="4aad1-182">En mode traité, le partage d’un partage **STGM \_ \_ Deny \_** de partage d’écriture ou de partage STGM peut améliorer les performances de manière significative, car il ne requiert pas d’instantanés. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="4aad1-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="4aad1-183">Pour plus d’informations sur les transactions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**\_partage STGM \_ exclusif**</span><span class="sxs-lookup"><span data-stu-id="4aad1-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="4aad1-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-186">Empêche d’autres utilisateurs d’ouvrir l’objet dans n’importe quel mode.</span><span class="sxs-lookup"><span data-stu-id="4aad1-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="4aad1-187">N’oubliez pas que cette valeur n’est pas une **opération de bits or simple** du **partage STGM refuser les valeurs d’écriture de refus de \_ \_ \_ lecture** et de **\_ partage \_ \_ STGM** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="4aad1-188">En mode traité, le partage d’un partage **STGM \_ \_ Deny \_** de partage d’écriture ou de partage STGM peut améliorer les performances de manière significative, car il ne requiert pas d’instantanés. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="4aad1-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="4aad1-189">Pour plus d’informations sur les transactions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_priorité STGM**</span><span class="sxs-lookup"><span data-stu-id="4aad1-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-192">Ouvre l’objet de stockage avec un accès exclusif à la version la plus récemment validée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="4aad1-193">Ainsi, les autres utilisateurs ne peuvent pas valider les modifications apportées à l’objet tant qu’il est ouvert en mode de priorité.</span><span class="sxs-lookup"><span data-stu-id="4aad1-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="4aad1-194">Vous obtenez des avantages en matière de performances pour les opérations de copie, mais vous empêchez les autres de valider les modifications.</span><span class="sxs-lookup"><span data-stu-id="4aad1-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="4aad1-195">Limitez le temps pendant lequel les objets sont ouverts en mode de priorité.</span><span class="sxs-lookup"><span data-stu-id="4aad1-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="4aad1-196">Vous devez spécifier **STGM \_ direct** et **STGM \_ Read** with Priority (mode de priorité) et vous ne pouvez pas spécifier **STGM \_ DELETEONRELEASE**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="4aad1-197">**STGM \_ DELETEONRELEASE** est valide uniquement lors de la création d’un objet racine, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="4aad1-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="4aad1-198">Elle n’est pas valide lors de l’ouverture d’un objet racine existant, par exemple avec [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="4aad1-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="4aad1-199">Elle n’est pas non plus valide lors de la création ou de l’ouverture d’un sous-élément, par exemple, avec [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span><span class="sxs-lookup"><span data-stu-id="4aad1-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ créer**</span><span class="sxs-lookup"><span data-stu-id="4aad1-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-202">Indique qu’un flux ou un objet de stockage existant doit être supprimé avant que le nouvel objet ne le remplace.</span><span class="sxs-lookup"><span data-stu-id="4aad1-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="4aad1-203">Un nouvel objet est créé lorsque cet indicateur est spécifié uniquement si l’objet existant a été supprimé avec succès.</span><span class="sxs-lookup"><span data-stu-id="4aad1-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="4aad1-204">Cet indicateur est utilisé lors de la tentative de création de :</span><span class="sxs-lookup"><span data-stu-id="4aad1-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="4aad1-205">Un objet de stockage sur un disque, mais il existe un fichier portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="4aad1-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="4aad1-206">Objet à l’intérieur d’un objet de stockage, mais il existe un objet portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="4aad1-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="4aad1-207">Objet de tableau d’octets, mais avec le nom spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="4aad1-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="4aad1-208">Cet indicateur ne peut pas être utilisé avec des opérations d’ouverture, telles que [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ou [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="4aad1-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertir**</span><span class="sxs-lookup"><span data-stu-id="4aad1-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-211">Crée le nouvel objet tout en conservant les données existantes dans un flux nommé « contents ».</span><span class="sxs-lookup"><span data-stu-id="4aad1-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="4aad1-212">Dans le cas d’un objet de stockage ou d’un tableau d’octets, les anciennes données sont mises en forme dans un flux, que le fichier ou le tableau d’octets existant contient actuellement un objet de stockage en couches.</span><span class="sxs-lookup"><span data-stu-id="4aad1-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="4aad1-213">Cet indicateur ne peut être utilisé que lors de la création d’un objet de stockage racine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="4aad1-214">Elle ne peut pas être utilisée dans un objet de stockage ; par exemple, dans [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="4aad1-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="4aad1-215">Il n’est pas non plus valide d’utiliser cet indicateur et l’indicateur **STGM \_ DELETEONRELEASE** simultanément.</span><span class="sxs-lookup"><span data-stu-id="4aad1-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="4aad1-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-217">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-218">Provoque l’échec de l’opération de création si un objet existant portant le nom spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="4aad1-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="4aad1-219">Dans ce cas, **STG \_ E \_ FILEALREADYEXISTS** est retourné.</span><span class="sxs-lookup"><span data-stu-id="4aad1-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="4aad1-220">Il s’agit du mode de création par défaut ; autrement dit, si aucun autre indicateur Create n’est spécifié, **STGM \_ FAILIFTHERE** est implicite.</span><span class="sxs-lookup"><span data-stu-id="4aad1-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ direct**</span><span class="sxs-lookup"><span data-stu-id="4aad1-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-222">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-223">Indique que, en mode direct, chaque modification apportée à un élément de stockage ou de flux est écrite telle qu’elle se produit.</span><span class="sxs-lookup"><span data-stu-id="4aad1-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="4aad1-224">Il s’agit de la valeur par défaut si aucune **STGM \_ directe** ni **STGM \_ traitée** n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ traité**</span><span class="sxs-lookup"><span data-stu-id="4aad1-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-227">Indique que, en mode traité, les modifications sont mises en mémoire tampon et écrites uniquement si une opération de validation explicite est appelée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="4aad1-228">Pour ignorer les modifications, appelez la méthode [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) dans l’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)ou [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .</span><span class="sxs-lookup"><span data-stu-id="4aad1-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="4aad1-229">L’implémentation de fichier composé COM de **IStorage** ne prend pas en charge les flux transactionnels, ce qui signifie que les flux ne peuvent être ouverts qu’en mode direct, et que vous ne pouvez pas annuler les modifications apportées, mais les stockages transactionnels sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4aad1-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="4aad1-230">Les implémentations de fichiers composés, autonomes et de système de fichiers NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ne prennent pas en charge les jeux de propriétés transactionnels, simples, car ces jeux de propriétés sont stockés dans des flux.</span><span class="sxs-lookup"><span data-stu-id="4aad1-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="4aad1-231">Toutefois, les transactions de jeux de propriétés qui peuvent être créés en spécifiant l’indicateur **PROPSETFLAG not \_ simple** dans le paramètre *grfFlags* de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4aad1-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOrayer**</span><span class="sxs-lookup"><span data-stu-id="4aad1-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-234">Indique que, en mode traité, un fichier de travail temporaire est généralement utilisé pour enregistrer les modifications jusqu’à ce que la méthode de **validation** soit appelée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="4aad1-235">La spécification de **STGM \_ noscratch** permet d’utiliser la partie inutilisée du fichier d’origine comme espace de travail au lieu de créer un fichier à cet effet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="4aad1-236">Cela n’affecte pas les données dans le fichier d’origine et, dans certains cas, les performances peuvent être améliorées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="4aad1-237">Il n’est pas possible de spécifier cet indicateur sans spécifier également **STGM \_ traité**, et cet indicateur ne peut être utilisé que dans une racine ouverte.</span><span class="sxs-lookup"><span data-stu-id="4aad1-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="4aad1-238">Pour plus d’informations sur le mode noscratch, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="4aad1-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-241">Cet indicateur est utilisé lors de l’ouverture d’un objet de stockage avec **STGM \_** et sans **\_ partage STGM partage \_ exclusif** ou **partage de STGM refus d' \_ \_ \_ écriture**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="4aad1-242">Dans ce cas, la spécification de **STGM \_ nosnapshot** empêche l’implémentation fournie par le système de créer une copie d’instantané du fichier.</span><span class="sxs-lookup"><span data-stu-id="4aad1-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="4aad1-243">Au lieu de cela, les modifications apportées au fichier sont écrites à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="4aad1-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="4aad1-244">L’espace inutilisé n’est pas récupéré à moins que la consolidation ne soit effectuée pendant la validation et qu’il n’y ait qu’un seul writer en cours sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="4aad1-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="4aad1-245">Lorsque le fichier est ouvert en mode sans instantané, une autre opération d’ouverture ne peut pas être effectuée sans spécifier **STGM \_ nosnapshot**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="4aad1-246">Cet indicateur ne peut être utilisé que dans une opération d’ouverture racine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="4aad1-247">Pour plus d’informations sur le mode nosnapshot, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ simple**</span><span class="sxs-lookup"><span data-stu-id="4aad1-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-250">Fournit une implémentation plus rapide d’un fichier composé dans un cas limité, mais fréquemment utilisé.</span><span class="sxs-lookup"><span data-stu-id="4aad1-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="4aad1-251">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ direct \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="4aad1-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-254">Prend en charge le mode direct pour les opérations de fichier multilecture et à rédacteur unique.</span><span class="sxs-lookup"><span data-stu-id="4aad1-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="4aad1-255">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4aad1-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="4aad1-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aad1-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="4aad1-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="4aad1-258">Indique que le fichier sous-jacent doit être détruit automatiquement lorsque l’objet de stockage racine est libéré.</span><span class="sxs-lookup"><span data-stu-id="4aad1-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="4aad1-259">Cette fonctionnalité est particulièrement utile pour créer des fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="4aad1-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="4aad1-260">Cet indicateur ne peut être utilisé que lors de la création d’un objet racine, par exemple avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="4aad1-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="4aad1-261">Elle n’est pas valide lors de l’ouverture d’un objet racine, par exemple avec [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), ou lors de la création ou de l’ouverture d’un sous-élément, par exemple, avec [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="4aad1-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="4aad1-262">Il n’est pas non plus valide d’utiliser cet indicateur et l' \_ indicateur STGM Convert simultanément.</span><span class="sxs-lookup"><span data-stu-id="4aad1-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aad1-263">Notes</span><span class="sxs-lookup"><span data-stu-id="4aad1-263">Remarks</span></span>

<span data-ttu-id="4aad1-264">Vous pouvez combiner ces indicateurs, mais vous ne pouvez choisir qu’un seul indicateur de chaque groupe d’indicateurs associés.</span><span class="sxs-lookup"><span data-stu-id="4aad1-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="4aad1-265">En général, un indicateur de chacun des groupes d’accès et de partage doit être spécifié pour toutes les fonctions et méthodes qui utilisent ces constantes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="4aad1-266">Les indicateurs d’autres groupes sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="4aad1-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="4aad1-267">Mode traité</span><span class="sxs-lookup"><span data-stu-id="4aad1-267">Transacted Mode</span></span>

<span data-ttu-id="4aad1-268">Lorsque l' **indicateur \_ direct STGM** est spécifié, une seule combinaison des indicateurs suivants peut être spécifiée à partir des groupes d’accès et de partage.</span><span class="sxs-lookup"><span data-stu-id="4aad1-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="4aad1-269">N’oubliez pas que le mode direct est implicite en l’absence de **\_ transaction STGM**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="4aad1-270">Autrement dit, si aucune **STGM \_ directe** ni **STGM \_ traitée** n’est spécifiée, **STGM \_ direct** est supposé.</span><span class="sxs-lookup"><span data-stu-id="4aad1-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="4aad1-271">Lorsque l’indicateur **STGM \_ traité** est spécifié, les objets sont créés ou ouverts en mode traité.</span><span class="sxs-lookup"><span data-stu-id="4aad1-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="4aad1-272">Dans ce mode, les modifications apportées à un objet ne sont pas conservées tant qu’elles ne sont pas validées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="4aad1-273">Par exemple, les modifications apportées à un objet de stockage transactionnel ne sont pas conservées tant que la méthode [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="4aad1-274">Les modifications apportées à un objet de stockage de ce type seront perdues si l’objet de stockage est libéré (version finale) avant l’appel de la méthode **Commit** ou si la méthode [**IStorage :: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) est appelée.</span><span class="sxs-lookup"><span data-stu-id="4aad1-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="4aad1-275">Lorsqu’un objet est créé ou ouvert en mode transactionnel, l’implémentation doit conserver les données d’origine et les mises à jour de ces données, afin que les mises à jour puissent être annulées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4aad1-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="4aad1-276">Cela s’effectue généralement en écrivant les modifications dans un espace de travail jusqu’à ce qu’elles soient validées, ou en créant une copie, appelée instantané, des données récemment validées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="4aad1-277">Lorsqu’un objet de stockage racine est ouvert en mode transactionnel, l’emplacement et le comportement des données de travail et des copies d’instantanés peuvent être contrôlés pour optimiser les performances avec les indicateurs **STGM \_ noéraflure** et **STGM \_ nosnapshot** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="4aad1-278">(Un objet de stockage racine est obtenu à partir de, par exemple, la fonction [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; un objet de stockage obtenu à partir de la méthode [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) est un objet de sous-stockage.) En règle générale, les captures instantanées et les données de travail sont stockées dans des fichiers temporaires, séparées du stockage.</span><span class="sxs-lookup"><span data-stu-id="4aad1-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="4aad1-279">L’effet de ces indicateurs dépend du nombre de lecteurs et/ou d’enregistreurs accédant au stockage racine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="4aad1-280">Dans le cas d’un seul rédacteur, un objet de stockage en mode transactionnel est ouvert pour l’accès en écriture et il ne peut pas y avoir d’autre accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="4aad1-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="4aad1-281">Autrement dit, le fichier est ouvert avec **STGM \_ traité**, l’accès à **STGM \_ Write** ou **STGM \_ ReadWrite** et le partage du **\_ partage STGM share \_ exclusif**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="4aad1-282">Dans ce cas, les modifications apportées à l’objet de stockage sont écrites dans la zone Scratch.</span><span class="sxs-lookup"><span data-stu-id="4aad1-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="4aad1-283">Lorsque ces modifications sont validées, elles sont copiées dans le stockage d’origine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="4aad1-284">Par conséquent, si aucune modification n’est apportée à l’objet de stockage, aucun transfert de données n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4aad1-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="4aad1-285">Dans le cas de « plusieurs rédacteurs », un objet de stockage traité est ouvert pour l’accès en écriture, mais il est partagé dans ce asway comme pour permettre à d’autres enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="4aad1-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="4aad1-286">Autrement dit, l’objet de stockage est ouvert **avec \_ STGM traité**, l’accès à **STGM \_ Write** ou **STGM \_ ReadWrite**, et le partage du **\_ partage STGM Deny est \_ \_ Read**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="4aad1-287">Si le partage **du \_ partage STGM \_ Deny \_ None** n’est pas spécifié, alors la casse est « multiple-Writer, multi-Reader ».</span><span class="sxs-lookup"><span data-stu-id="4aad1-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="4aad1-288">Dans ce cas, une capture instantanée des données d’origine est effectuée pendant l’opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="4aad1-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="4aad1-289">Par conséquent, même si aucune modification n’est apportée au stockage et/ou qu’elle n’est pas réellement ouverte par un autre writer simultanément, le transfert de données est toujours nécessaire lors de l’ouverture.</span><span class="sxs-lookup"><span data-stu-id="4aad1-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="4aad1-290">Par conséquent, il est possible d’obtenir les meilleures performances d’ouverture en ouvrant l’objet de stockage dans **STGM \_ partage \_ refuser l' \_ écriture** ou partager des STGM en mode **\_ \_ exclusif** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="4aad1-291">Pour plus d’informations sur la façon dont les modifications sont validées lorsqu’il y a plusieurs Writers, consultez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="4aad1-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="4aad1-292">Dans le cas d’un « writer unique, à plusieurs lecteurs », un objet de stockage traité est ouvert pour l’accès en écriture, mais il est partagé avec les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="4aad1-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="4aad1-293">Autrement dit, l’objet de stockage est ouvert par l’enregistreur **avec \_ STGM traité**, l’accès à **STGM \_ ReadWrite** ou **STGM \_ Write**, et le partage du **\_ partage STGM refuse l' \_ \_ écriture**.</span><span class="sxs-lookup"><span data-stu-id="4aad1-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="4aad1-294">Le stockage est ouvert par les lecteurs avec les **STGM \_ traités**, l’accès à **STGM \_ Read** et le partage du **\_ partage STGM \_ \_** ne sont pas associés.</span><span class="sxs-lookup"><span data-stu-id="4aad1-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="4aad1-295">Dans ce cas, le writer utilise la zone Scratch pour stocker les modifications non validées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="4aad1-296">Comme dans les cas ci-dessus, le lecteur entraîne une pénalité de performance à l’heure d’ouverture pendant la création d’une copie d’instantané des données.</span><span class="sxs-lookup"><span data-stu-id="4aad1-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="4aad1-297">En règle générale, la zone Scratch est un fichier temporaire distinct des données d’origine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="4aad1-298">Lorsque des modifications sont validées dans le fichier d’origine, les données doivent être transférées à partir du fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="4aad1-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="4aad1-299">Pour éviter ce transfert de données, l’indicateur **\_ noscratch STGM** peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="4aad1-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="4aad1-300">Lorsque cet indicateur est spécifié, des parties du fichier d’objet de stockage sont utilisées pour la zone Scratch, plutôt que pour un fichier temporaire distinct.</span><span class="sxs-lookup"><span data-stu-id="4aad1-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="4aad1-301">Par conséquent, la validation des modifications peut être effectuée rapidement, car un faible transfert de données est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4aad1-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="4aad1-302">L’inconvénient est que le fichier de stockage peut devenir plus volumineux qu’il ne le serait, car il doit être augmenté pour être suffisamment grand pour les données d’origine et la zone de travail.</span><span class="sxs-lookup"><span data-stu-id="4aad1-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="4aad1-303">Pour consolider les données et supprimer cette zone superflue, rouvrez le stockage racine en mode traité, mais sans définir l’indicateur **\_ noscratch STGM** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="4aad1-304">Ensuite, appelez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) avec l' **indicateur \_ consolider STGC** défini.</span><span class="sxs-lookup"><span data-stu-id="4aad1-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="4aad1-305">La zone d’instantané, comme la zone Scratch, est également, en général, un fichier temporaire, ce qui peut aussi être affecté par un indicateur STGM.</span><span class="sxs-lookup"><span data-stu-id="4aad1-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="4aad1-306">En spécifiant l’indicateur **STGM \_ nosnapshot** , un fichier d’instantané temporaire distinct n’est pas créé.</span><span class="sxs-lookup"><span data-stu-id="4aad1-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="4aad1-307">Au lieu de cela, les données d’origine ne sont jamais modifiées, même s’il existe un ou plusieurs enregistreurs par objet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="4aad1-308">Lorsque des modifications sont validées, elles sont ajoutées au fichier, mais les données d’origine restent intactes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="4aad1-309">Ce mode augmente l’efficacité, car il réduit le temps d’exécution en éliminant la nécessité de créer un instantané lors de l’opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="4aad1-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="4aad1-310">Toutefois, l’utilisation de ce mode peut aboutir à un fichier de stockage très volumineux, car les données du fichier ne peuvent jamais être remplacées.</span><span class="sxs-lookup"><span data-stu-id="4aad1-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="4aad1-311">Il n’y a aucune limite à la taille des fichiers ouverts en mode nosnapshot.</span><span class="sxs-lookup"><span data-stu-id="4aad1-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="4aad1-312">Mode de rédacteur direct, Multiple-Reader</span><span class="sxs-lookup"><span data-stu-id="4aad1-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="4aad1-313">Comme décrit, il est possible d’avoir un seul Writer et plusieurs lecteurs d’un objet de stockage, si cet objet est ouvert en mode traité.</span><span class="sxs-lookup"><span data-stu-id="4aad1-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="4aad1-314">Il est également possible d’obtenir le cas d’un seul writer en mode direct, en spécifiant l’indicateur **STGM \_ direct \_ SWMR** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="4aad1-315">En mode **STGM \_ direct \_ SWMR** , il est possible pour un appelant d’ouvrir un objet pour l’accès en lecture/écriture, tandis que d’autres appellent simultanément le fichier ouvert pour l’accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4aad1-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="4aad1-316">L’utilisation de cet indicateur n’est pas valide en association avec l’indicateur **STGM \_ traité** .</span><span class="sxs-lookup"><span data-stu-id="4aad1-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="4aad1-317">Dans ce mode, le writer ouvre l’objet avec les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4aad1-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="4aad1-318">**STGM \_ DIRECT \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**</span><span class="sxs-lookup"><span data-stu-id="4aad1-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="4aad1-319">et chacun des lecteurs ouvre l’objet avec les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4aad1-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="4aad1-320">**STGM \_ DIRECT \_ SWMR** \| **STGM \_ lire** \| **STGM \_ partager \_ refuser \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="4aad1-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="4aad1-321">Dans ce mode, pour modifier l’objet de stockage, l’enregistreur doit bénéficier d’un accès exclusif à l’objet.</span><span class="sxs-lookup"><span data-stu-id="4aad1-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="4aad1-322">Cela est possible lorsque tous les lecteurs l’ont fermé.</span><span class="sxs-lookup"><span data-stu-id="4aad1-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="4aad1-323">Le writer utilise l’interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) pour obtenir cet accès exclusif.</span><span class="sxs-lookup"><span data-stu-id="4aad1-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="4aad1-324">Mode simple</span><span class="sxs-lookup"><span data-stu-id="4aad1-324">Simple Mode</span></span>

<span data-ttu-id="4aad1-325">Le mode simple (**STGM \_ simple**) est utile pour les applications qui effectuent des opérations de sauvegarde complètes.</span><span class="sxs-lookup"><span data-stu-id="4aad1-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="4aad1-326">Elle est efficace, mais elle présente les contraintes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4aad1-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="4aad1-327">Il n’existe aucune prise en charge pour les sous-stockages.</span><span class="sxs-lookup"><span data-stu-id="4aad1-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="4aad1-328">L’objet de stockage et les objets de flux obtenus à partir de celui-ci ne peuvent pas être marshalés.</span><span class="sxs-lookup"><span data-stu-id="4aad1-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="4aad1-329">Chaque flux a une taille minimale.</span><span class="sxs-lookup"><span data-stu-id="4aad1-329">Each stream has a minimum size.</span></span> <span data-ttu-id="4aad1-330">Si le nombre minimal d’octets est écrit dans un flux lorsque le flux est libéré, le flux est étendu à la taille minimale.</span><span class="sxs-lookup"><span data-stu-id="4aad1-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="4aad1-331">Par exemple, la taille minimale d’une implémentation [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) particulière est de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="4aad1-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="4aad1-332">Un flux est créé et 1 Ko y est écrit.</span><span class="sxs-lookup"><span data-stu-id="4aad1-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="4aad1-333">À la version finale de cet **IStream**, la taille du flux sera automatiquement étendue à 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="4aad1-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="4aad1-334">Par la suite, l’ouverture du flux et l’appel de la méthode [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) affichent une taille de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="4aad1-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="4aad1-335">Les méthodes de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ne seront pas toutes prises en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4aad1-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="4aad1-336">Pour plus d’informations, consultez la rubrique relative [à l’implémentation d’un fichier composé IStorage](istorage-compound-file-implementation.md)et à l' [implémentation d’un fichier composé IStream](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4aad1-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="4aad1-337">Le [marshaling](/windows/desktop/Midl/marshaling-ole-data-types) est le processus d’empaquetage, de empaquetage et d’envoi de paramètres de méthode d’interface à travers des limites de thread ou de processus au sein d’un appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="4aad1-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="4aad1-338">Pour plus d’informations, consultez [Détails du marshaling](../com/marshaling-details.md) et [marshaling](../com/interface-marshaling.md)de l’interface.</span><span class="sxs-lookup"><span data-stu-id="4aad1-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="4aad1-339">Lorsqu’un objet de stockage est obtenu par une opération de création en mode simple :</span><span class="sxs-lookup"><span data-stu-id="4aad1-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="4aad1-340">Vous pouvez créer des éléments de flux, mais pas les ouvrir.</span><span class="sxs-lookup"><span data-stu-id="4aad1-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="4aad1-341">Lorsqu’un élément de flux est créé en appelant [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), il n’est pas possible de créer un autre flux tant que cet objet de flux n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="4aad1-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="4aad1-342">Une fois tous les flux écrits, appelez [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) pour vider les modifications.</span><span class="sxs-lookup"><span data-stu-id="4aad1-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="4aad1-343">Lorsqu’un objet de stockage est obtenu par une opération d’ouverture en mode simple :</span><span class="sxs-lookup"><span data-stu-id="4aad1-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="4aad1-344">Il est possible d’ouvrir un seul élément de flux à la fois.</span><span class="sxs-lookup"><span data-stu-id="4aad1-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="4aad1-345">Il n’est pas possible de modifier la taille d’un flux en appelant la méthode [**IStream :: assets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) ou en recherchant ou en écrivant au-delà de la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="4aad1-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="4aad1-346">Toutefois, étant donné que tous les flux ont une taille minimale, il est possible d’utiliser le flux jusqu’à cette taille, même si moins de données ont été écrites à l’origine.</span><span class="sxs-lookup"><span data-stu-id="4aad1-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="4aad1-347">Pour déterminer la taille d’un flux, utilisez la méthode [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .</span><span class="sxs-lookup"><span data-stu-id="4aad1-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="4aad1-348">Sachez que, si un élément de stockage est modifié par un objet de stockage qui n’est pas en mode simple, il n’est pas possible, encore une fois, d’ouvrir cet élément de stockage en mode simple.</span><span class="sxs-lookup"><span data-stu-id="4aad1-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aad1-349">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aad1-349">Requirements</span></span>



| <span data-ttu-id="4aad1-350">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aad1-350">Requirement</span></span> | <span data-ttu-id="4aad1-351">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aad1-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4aad1-352">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aad1-352">Minimum supported client</span></span><br/> | <span data-ttu-id="4aad1-353">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aad1-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4aad1-354">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aad1-354">Minimum supported server</span></span><br/> | <span data-ttu-id="4aad1-355">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aad1-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4aad1-356">En-tête</span><span class="sxs-lookup"><span data-stu-id="4aad1-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aad1-357"><dt>ObjBase. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aad1-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aad1-358">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aad1-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aad1-359">**ISequentialStream :: Read**</span><span class="sxs-lookup"><span data-stu-id="4aad1-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="4aad1-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="4aad1-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="4aad1-361">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="4aad1-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="4aad1-362">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4aad1-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="4aad1-363">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="4aad1-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="4aad1-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="4aad1-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="4aad1-365">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="4aad1-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="4aad1-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4aad1-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

