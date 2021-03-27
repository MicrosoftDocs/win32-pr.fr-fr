---
description: Cette classe est la classe de type d’événement pour les événements d’attente ALPC pour la réponse. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: Classe ALPC_Wait_For_Reply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972238"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="c01b5-104">\_Attente ALPC \_ pour la \_ classe reply</span><span class="sxs-lookup"><span data-stu-id="c01b5-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="c01b5-105">Cette classe est la classe de type d’événement pour les événements d’attente ALPC pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="c01b5-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="c01b5-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c01b5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c01b5-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="c01b5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c01b5-108">Members</span></span>

<span data-ttu-id="c01b5-109">La classe d' **\_ attente ALPC pour la \_ \_ réponse** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c01b5-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="c01b5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c01b5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c01b5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c01b5-111">Properties</span></span>

<span data-ttu-id="c01b5-112">La **classe \_ d’attente ALPC \_ pour la \_ réponse** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c01b5-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c01b5-113">**ID**</span><span class="sxs-lookup"><span data-stu-id="c01b5-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c01b5-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c01b5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c01b5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c01b5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c01b5-116">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="c01b5-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c01b5-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c01b5-117">Requirements</span></span>



| <span data-ttu-id="c01b5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c01b5-118">Requirement</span></span> | <span data-ttu-id="c01b5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c01b5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c01b5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c01b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c01b5-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c01b5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c01b5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c01b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c01b5-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c01b5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




