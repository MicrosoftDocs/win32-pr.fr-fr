---
description: Cette classe est la classe de type d’événement pour les événements d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528653"
---
# <a name="image_load-class"></a><span data-ttu-id="5e4d7-104">Classe de chargement d’image \_</span><span class="sxs-lookup"><span data-stu-id="5e4d7-104">Image\_Load class</span></span>

<span data-ttu-id="5e4d7-105">Cette classe est la classe de type d’événement pour les événements d’image.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="5e4d7-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e4d7-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="5e4d7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5e4d7-108">Members</span></span>

<span data-ttu-id="5e4d7-109">La classe de **\_ chargement d’image** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5e4d7-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="5e4d7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e4d7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e4d7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e4d7-111">Properties</span></span>

<span data-ttu-id="5e4d7-112">La classe de **\_ chargement d’image** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e4d7-113">DefaultBase</span><span class="sxs-lookup"><span data-stu-id="5e4d7-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-116">Qualificateurs : WmiDataId (7), pointeur</span><span class="sxs-lookup"><span data-stu-id="5e4d7-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-117">Adresse de base par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-118">FileName</span><span class="sxs-lookup"><span data-stu-id="5e4d7-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-121">Qualificateurs : WmiDataId (12), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="5e4d7-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-122">Nom de fichier et extension de la DLL ou de l’image exécutable.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-123">ImageBase</span><span class="sxs-lookup"><span data-stu-id="5e4d7-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-126">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="5e4d7-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-127">Adresse de base de l’application dans laquelle l’image est chargée.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-128">ImageCheckSum</span><span class="sxs-lookup"><span data-stu-id="5e4d7-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-131">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-132">Somme de contrôle d’image.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="5e4d7-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-136">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="5e4d7-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-137">Taille de l’image en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-137">Size of the image being loaded.</span></span>

<span data-ttu-id="5e4d7-138">Lors de l’utilisation de cette propriété, le type de données de cette propriété est taille \_ t.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="5e4d7-139">Le qualificateur de pointeur est utilisé pour déterminer si la taille \_ t est de 4 octets ou de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="5e4d7-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-143">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-144">Identifie le processus dans lequel l’image est chargée.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="5e4d7-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-148">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-149">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="5e4d7-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-153">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-154">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="5e4d7-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-158">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-159">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="5e4d7-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-163">Qualificateurs : WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-164">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="5e4d7-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-168">Qualificateurs : WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-169">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5e4d7-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="5e4d7-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e4d7-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e4d7-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e4d7-173">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="5e4d7-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="5e4d7-174">Heure et date auxquelles l’image a été chargée ou déchargée.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e4d7-175">Notes</span><span class="sxs-lookup"><span data-stu-id="5e4d7-175">Remarks</span></span>

<span data-ttu-id="5e4d7-176">Les événements DCStart et DCEnd énumèrent toutes les images chargées au début et à la fin de la trace, respectivement.</span><span class="sxs-lookup"><span data-stu-id="5e4d7-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4d7-177">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e4d7-177">Requirements</span></span>



| <span data-ttu-id="5e4d7-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e4d7-178">Requirement</span></span> | <span data-ttu-id="5e4d7-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e4d7-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e4d7-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e4d7-180">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4d7-181">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e4d7-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e4d7-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e4d7-182">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4d7-183">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e4d7-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e4d7-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e4d7-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4d7-185">**Image**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="5e4d7-186">**Image \_ v0**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="5e4d7-187">**Image \_ v1**</span><span class="sxs-lookup"><span data-stu-id="5e4d7-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




