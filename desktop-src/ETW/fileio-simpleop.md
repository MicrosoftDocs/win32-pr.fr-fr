---
description: Cette classe est la classe de type d’événement pour les événements d’opération de fichier simples. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Classe FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973554"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="734f9-104">FileIo \_ SimpleOp, classe</span><span class="sxs-lookup"><span data-stu-id="734f9-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="734f9-105">Cette classe est la classe de type d’événement pour les événements d’opération de fichier simples.</span><span class="sxs-lookup"><span data-stu-id="734f9-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="734f9-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="734f9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="734f9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="734f9-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="734f9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="734f9-108">Members</span></span>

<span data-ttu-id="734f9-109">La classe **FileIo \_ SimpleOp** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="734f9-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="734f9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="734f9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="734f9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="734f9-111">Properties</span></span>

<span data-ttu-id="734f9-112">La classe **FileIo \_ SimpleOp** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="734f9-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="734f9-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="734f9-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="734f9-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="734f9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="734f9-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="734f9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="734f9-116">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="734f9-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="734f9-117">Pour déterminer le nom de fichier, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="734f9-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="734f9-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="734f9-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="734f9-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="734f9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="734f9-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="734f9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="734f9-121">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="734f9-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="734f9-122">Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.</span><span class="sxs-lookup"><span data-stu-id="734f9-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="734f9-123">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="734f9-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="734f9-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="734f9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="734f9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="734f9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="734f9-126">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="734f9-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="734f9-127">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="734f9-127">IO request packet.</span></span> <span data-ttu-id="734f9-128">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="734f9-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="734f9-129">**TTID**</span><span class="sxs-lookup"><span data-stu-id="734f9-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="734f9-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="734f9-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="734f9-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="734f9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="734f9-132">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="734f9-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="734f9-133">Identificateur du thread qui effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="734f9-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="734f9-134">Notes</span><span class="sxs-lookup"><span data-stu-id="734f9-134">Remarks</span></span>

<span data-ttu-id="734f9-135">L’événement Cleanup est journalisé lorsque le dernier handle du fichier est fermé.</span><span class="sxs-lookup"><span data-stu-id="734f9-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="734f9-136">L’événement Close spécifie qu’un objet fichier est en cours de libération.</span><span class="sxs-lookup"><span data-stu-id="734f9-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="734f9-137">L’événement Flush spécifie quand les mémoires tampons de fichier sont entièrement vidées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="734f9-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="734f9-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="734f9-138">Requirements</span></span>



| <span data-ttu-id="734f9-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="734f9-139">Requirement</span></span> | <span data-ttu-id="734f9-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="734f9-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="734f9-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="734f9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="734f9-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="734f9-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="734f9-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="734f9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="734f9-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="734f9-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="734f9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="734f9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="734f9-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="734f9-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




