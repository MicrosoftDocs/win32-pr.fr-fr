---
description: La classe CMediaType gère les types de média. Cette classe hérite de la \_ structure du type de média am \_ . Il peut être casté en une variable de type de \_ média am \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: CMediaType, classe (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523987"
---
# <a name="cmediatype-class"></a><span data-ttu-id="2ff2c-105">CMediaType, classe</span><span class="sxs-lookup"><span data-stu-id="2ff2c-105">CMediaType class</span></span>

![hiérarchie de la classe cmediatype](images/mtype01.png)

<span data-ttu-id="2ff2c-107">La `CMediaType` classe gère les types de média.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="2ff2c-108">Cette classe hérite de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="2ff2c-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="2ff2c-109">Il peut être casté en une variable de type de **\_ média \_ am**.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="2ff2c-110">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="2ff2c-110">Public Methods</span></span>                                                      | <span data-ttu-id="2ff2c-111">Description</span><span class="sxs-lookup"><span data-stu-id="2ff2c-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2ff2c-112">**CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="2ff2c-113">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="2ff2c-114">**~ CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="2ff2c-115">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="2ff2c-116">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="2ff2c-117">Définit le type de média à partir d’un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="2ff2c-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="2ff2c-119">Détermine si un type principal a été assigné à cet objet.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="2ff2c-120">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="2ff2c-121">Récupère le type principal.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="2ff2c-122">**SetType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="2ff2c-123">Spécifie le type principal.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="2ff2c-124">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="2ff2c-125">Récupère le sous-type.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="2ff2c-126">**SetSubtype**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="2ff2c-127">Spécifie le sous-type.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="2ff2c-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="2ff2c-129">Détermine si les échantillons ont une taille fixe ou une taille variable.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="2ff2c-130">**IsTemporalCompressed**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="2ff2c-131">Détermine si le flux utilise la compression temporelle.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="2ff2c-132">**GetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="2ff2c-133">Récupère la taille de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="2ff2c-134">**SetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="2ff2c-135">Spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="2ff2c-136">**SetVariableSize**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="2ff2c-137">Spécifie que les exemples n’ont pas de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="2ff2c-138">**SetTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="2ff2c-139">Spécifie si les échantillons sont compressés à l’aide de la compression temporelle.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="2ff2c-140">**Format**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="2ff2c-141">Récupère un pointeur vers le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="2ff2c-142">**FormatLength**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="2ff2c-143">Récupère la longueur du bloc de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="2ff2c-144">**SetFormatType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="2ff2c-145">Spécifie le type de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="2ff2c-146">**FormatType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="2ff2c-147">Récupère le type de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="2ff2c-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="2ff2c-149">Spécifie le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="2ff2c-150">**ResetFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="2ff2c-151">Supprime le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="2ff2c-152">**AllocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="2ff2c-153">Alloue de la mémoire pour le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="2ff2c-154">**ReallocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="2ff2c-155">Réaffecte le bloc de format à une nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="2ff2c-156">**InitMediaType**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="2ff2c-157">Initialise le type de média.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="2ff2c-158">**MatchesPartial**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="2ff2c-159">Détermine si ce type de média correspond à un type de média partiellement spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="2ff2c-160">**IsPartiallySpecified**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="2ff2c-161">Détermine si le type de média est partiellement défini.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="2ff2c-162">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="2ff2c-162">Operators</span></span>                                                           | <span data-ttu-id="2ff2c-163">Description</span><span class="sxs-lookup"><span data-stu-id="2ff2c-163">Description</span></span>                                                                    |
| [<span data-ttu-id="2ff2c-164">**opérateur =**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="2ff2c-165">Surcharge l’opérateur d’assignation pour copier un type de média.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="2ff2c-166">**opérateur = =**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="2ff2c-167">Vérifie l’égalité d’objets `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="2ff2c-168">**opérateur ! =**</span><span class="sxs-lookup"><span data-stu-id="2ff2c-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="2ff2c-169">Vérifie l’inégalité d’objets `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="2ff2c-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="2ff2c-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ff2c-170">Requirements</span></span>



| <span data-ttu-id="2ff2c-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ff2c-171">Requirement</span></span> | <span data-ttu-id="2ff2c-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ff2c-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff2c-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ff2c-173">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff2c-174"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2c-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2ff2c-175">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2ff2c-175">Library</span></span><br/> | <dl> <span data-ttu-id="2ff2c-176"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2c-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




