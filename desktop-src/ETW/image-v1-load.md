---
description: Cette classe est la classe de type d’événement pour les événements de chargement d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Classe Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971931"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="ddcb3-104">\_Classe de \_ charge image v1</span><span class="sxs-lookup"><span data-stu-id="ddcb3-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="ddcb3-105">Cette classe est la classe de type d’événement pour les événements de chargement d’image.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="ddcb3-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddcb3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddcb3-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="ddcb3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ddcb3-108">Members</span></span>

<span data-ttu-id="ddcb3-109">La **classe \_ \_ Load de l’image v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddcb3-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="ddcb3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddcb3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddcb3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ddcb3-111">Properties</span></span>

<span data-ttu-id="ddcb3-112">La classe de **\_ \_ chargement image v1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddcb3-113">FileName</span><span class="sxs-lookup"><span data-stu-id="ddcb3-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddcb3-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ddcb3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddcb3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-116">Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="ddcb3-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ddcb3-117">Nom de fichier et extension de la DLL ou de l’image exécutable à charger.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="ddcb3-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="ddcb3-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddcb3-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddcb3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddcb3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="ddcb3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ddcb3-122">Adresse de base de l’application dans laquelle l’image est chargée.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ddcb3-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="ddcb3-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddcb3-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddcb3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddcb3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-126">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="ddcb3-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ddcb3-127">Taille de l’image en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-127">Size of the image being loaded.</span></span>

<span data-ttu-id="ddcb3-128">Lors de l’utilisation de cette propriété, le type de données de cette propriété est taille \_ t.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="ddcb3-129">Le qualificateur de pointeur est utilisé pour déterminer si la taille \_ t est de 4 octets ou de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ddcb3-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="ddcb3-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddcb3-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddcb3-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ddcb3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddcb3-133">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="ddcb3-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ddcb3-134">Identifie le processus dans lequel l’image est chargée.</span><span class="sxs-lookup"><span data-stu-id="ddcb3-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddcb3-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ddcb3-135">Requirements</span></span>



| <span data-ttu-id="ddcb3-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddcb3-136">Requirement</span></span> | <span data-ttu-id="ddcb3-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddcb3-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ddcb3-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddcb3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ddcb3-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddcb3-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ddcb3-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddcb3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ddcb3-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddcb3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddcb3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddcb3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddcb3-143">**Image \_ v1**</span><span class="sxs-lookup"><span data-stu-id="ddcb3-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




