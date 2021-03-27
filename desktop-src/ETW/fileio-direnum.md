---
description: Cette classe est la classe de type d’événement pour les événements d’énumération de notifications de répertoires et de répertoires. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: Classe FileIo_DirEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972202"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="af89a-104">FileIo \_ DirEnum, classe</span><span class="sxs-lookup"><span data-stu-id="af89a-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="af89a-105">Cette classe est la classe de type d’événement pour les événements d’énumération de notifications de répertoires et de répertoires.</span><span class="sxs-lookup"><span data-stu-id="af89a-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="af89a-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="af89a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af89a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af89a-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="af89a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="af89a-108">Members</span></span>

<span data-ttu-id="af89a-109">La classe **FileIo \_ DirEnum** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="af89a-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="af89a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af89a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af89a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af89a-111">Properties</span></span>

<span data-ttu-id="af89a-112">La classe **FileIo \_ DirEnum** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="af89a-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af89a-113">**FileIndex**</span><span class="sxs-lookup"><span data-stu-id="af89a-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-116">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="af89a-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="af89a-117">Index de fichier à partir duquel continuer l’énumération de répertoires.</span><span class="sxs-lookup"><span data-stu-id="af89a-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-118">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="af89a-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-121">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="af89a-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af89a-122">Pour déterminer le nom du répertoire, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="af89a-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="af89a-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af89a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-126">Qualificateurs : WmiDataId (8), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="af89a-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="af89a-127">Modèle spécifié pour l’énumération de répertoires.</span><span class="sxs-lookup"><span data-stu-id="af89a-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-128">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="af89a-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-131">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="af89a-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af89a-132">Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.</span><span class="sxs-lookup"><span data-stu-id="af89a-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-133">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="af89a-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-136">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="af89a-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af89a-137">Classe d’informations d’énumération de répertoire demandée.</span><span class="sxs-lookup"><span data-stu-id="af89a-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-138">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="af89a-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-141">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="af89a-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af89a-142">Paquet de demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="af89a-142">IO request packet.</span></span> <span data-ttu-id="af89a-143">Cette propriété identifie l’activité d’e/s.</span><span class="sxs-lookup"><span data-stu-id="af89a-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-144">**Durée**</span><span class="sxs-lookup"><span data-stu-id="af89a-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-147">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="af89a-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="af89a-148">Taille de la mémoire tampon de requête, en octets.</span><span class="sxs-lookup"><span data-stu-id="af89a-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="af89a-149">**TTID**</span><span class="sxs-lookup"><span data-stu-id="af89a-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af89a-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af89a-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af89a-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af89a-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af89a-152">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="af89a-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="af89a-153">Identificateur du thread qui effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="af89a-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af89a-154">Notes</span><span class="sxs-lookup"><span data-stu-id="af89a-154">Remarks</span></span>

<span data-ttu-id="af89a-155">L’énumération de répertoires et les événements de notification d’annuaire sont enregistrés lorsqu’un répertoire est énuméré ou lorsqu’une notification de modification de répertoire est envoyée aux écouteurs inscrits, respectivement.</span><span class="sxs-lookup"><span data-stu-id="af89a-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="af89a-156">Spécifications</span><span class="sxs-lookup"><span data-stu-id="af89a-156">Requirements</span></span>



| <span data-ttu-id="af89a-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af89a-157">Requirement</span></span> | <span data-ttu-id="af89a-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="af89a-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af89a-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af89a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="af89a-160">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af89a-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af89a-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af89a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="af89a-162">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af89a-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af89a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af89a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af89a-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="af89a-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




