---
description: Cette classe est la classe de type d’événement pour le chargement d’image dans les événements de fichier d’échange. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973415"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="f8ed1-104">PageFault \_ ImageLoadBacked, classe</span><span class="sxs-lookup"><span data-stu-id="f8ed1-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="f8ed1-105">Cette classe est la classe de type d’événement pour le chargement d’image dans les événements de fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="f8ed1-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ed1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8ed1-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="f8ed1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f8ed1-108">Members</span></span>

<span data-ttu-id="f8ed1-109">La classe **PageFault \_ ImageLoadBacked** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8ed1-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="f8ed1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8ed1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8ed1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8ed1-111">Properties</span></span>

<span data-ttu-id="f8ed1-112">La classe **PageFault \_ ImageLoadBacked** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8ed1-113">**DeviceChar**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8ed1-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8ed1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-116">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8ed1-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8ed1-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f8ed1-118">**FileChar**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8ed1-119">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8ed1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-121">Qualificateurs : WmiDataId (3), format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8ed1-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8ed1-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f8ed1-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8ed1-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8ed1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-126">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="f8ed1-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f8ed1-127">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f8ed1-128">**LoadFlags**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8ed1-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8ed1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8ed1-131">Qualificateurs : WmiDataId (4), format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8ed1-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8ed1-132">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8ed1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f8ed1-133">Remarks</span></span>

<span data-ttu-id="f8ed1-134">L’événement est enregistré lors de la création d’une section d’image (par exemple, un chargement de DLL) lorsque le gestionnaire de mémoire détermine que l’image doit être copiée et exécutée à partir du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="f8ed1-135">En règle générale, les images sont exécutées à partir du fichier source, mais la sauvegarde du fichier d’échange peut se produire lorsque le gestionnaire de mémoire détermine que le fichier source peut être modifié de façon asynchrone par des Writers existants ou lorsque le fichier source se trouve sur un support amovible ou un périphérique distant.</span><span class="sxs-lookup"><span data-stu-id="f8ed1-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ed1-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8ed1-136">Requirements</span></span>



| <span data-ttu-id="f8ed1-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8ed1-137">Requirement</span></span> | <span data-ttu-id="f8ed1-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8ed1-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f8ed1-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8ed1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ed1-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8ed1-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f8ed1-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8ed1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ed1-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8ed1-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8ed1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8ed1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ed1-144">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="f8ed1-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




