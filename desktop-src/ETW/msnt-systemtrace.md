---
description: Classe parente à partir de laquelle toutes les classes de trace d’événements système sont dérivées. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972282"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="8efdf-104">MSNT \_ SystemTrace, classe</span><span class="sxs-lookup"><span data-stu-id="8efdf-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="8efdf-105">Classe parente à partir de laquelle toutes les classes de trace d’événements système sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="8efdf-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="8efdf-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="8efdf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8efdf-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="8efdf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8efdf-108">Members</span></span>

<span data-ttu-id="8efdf-109">La classe **MSNT \_ SystemTrace** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8efdf-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="8efdf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8efdf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8efdf-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8efdf-111">Properties</span></span>

<span data-ttu-id="8efdf-112">La classe **MSNT \_ SystemTrace** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8efdf-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8efdf-113">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="8efdf-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8efdf-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8efdf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8efdf-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8efdf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8efdf-116">Qualificateurs : **DefineValues {"processus de l’indicateur de trace d’événements", "thread de l’indicateur de trace d’événements", "chargement de l’image de l’indicateur de trace d’événements", "compteurs de processus de l’indicateur de trace d’événements", "indicateur de trace d’événements \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ CSWITCH", "indicateur de trace d’événements \_ \_ \_ DPC", "indicateur de trace d’événements indicateur de trace d’événements \_ \_ \_ \_ \_ \_ SYSTEMCALL", "indicateur de trace d’événements \_ \_ \_ Disk \_ IO", "Event \_ trace \_ Flag Disk \_ \_ file \_ IO", "Event \_ trace \_ Flag \_ Disk \_ IO \_ init", "EVENT trace Flag répartiteur", "EVENT trace Flag Network tcpips", "Event Trace Flag \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Memory \_ \_ Faults", "Event \_ trace Flag virtuel Alloc", "Event Trace Flag \_ \_ \_ \_ \_ \_ Network \_ tcpip", "Event \_ trace Flag \_ \_ Registry», « Event Trace Flag \_ \_ \_ ALPC », « Event \_ trace \_ Flag \_ Split \_ IO », « Event \_ trace \_ Flag \_ Driver », « Event Trace Flag \_ \_ \_ Profile », « Event \_ trace \_ Flag \_ file \_ IO », «Event \_ trace \_ Flag \_ file \_ IO \_ init"}**, **ValueMap {"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100" , « 0x00000200 », « 0x00000400 », « 0x00000800 », « 0x00001000 », « 0x00002000 », « 0x00004000** », « 0x00010000 », « 0x00020000 », « 0x00100000 », « 0x00200000 », « 0x00800000 », « 0x01000000 », « 0x02000000 », « 0x04000000 »}</span><span class="sxs-lookup"><span data-stu-id="8efdf-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="8efdf-117">Activez l’indicateur qui indique les fournisseurs de noyau activés.</span><span class="sxs-lookup"><span data-stu-id="8efdf-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8efdf-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8efdf-118">Requirements</span></span>



| <span data-ttu-id="8efdf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8efdf-119">Requirement</span></span> | <span data-ttu-id="8efdf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8efdf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8efdf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8efdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8efdf-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8efdf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8efdf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8efdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8efdf-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8efdf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




