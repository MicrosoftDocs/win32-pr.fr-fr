---
description: Cette classe est la classe de type d’événement pour les événements de message de réception ALPC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Classe ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972246"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="890cf-104">Classe de message de \_ réception ALPC \_</span><span class="sxs-lookup"><span data-stu-id="890cf-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="890cf-105">Cette classe est la classe de type d’événement pour les événements de message de réception ALPC.</span><span class="sxs-lookup"><span data-stu-id="890cf-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="890cf-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="890cf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="890cf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="890cf-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="890cf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="890cf-108">Members</span></span>

<span data-ttu-id="890cf-109">La classe de **\_ \_ message de réception ALPC** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="890cf-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="890cf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="890cf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="890cf-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="890cf-111">Properties</span></span>

<span data-ttu-id="890cf-112">La classe de **\_ \_ message de réception ALPC** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="890cf-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="890cf-113">**ID**</span><span class="sxs-lookup"><span data-stu-id="890cf-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890cf-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="890cf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="890cf-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="890cf-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="890cf-116">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="890cf-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="890cf-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="890cf-117">Requirements</span></span>



| <span data-ttu-id="890cf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="890cf-118">Requirement</span></span> | <span data-ttu-id="890cf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="890cf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="890cf-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="890cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="890cf-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="890cf-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="890cf-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="890cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="890cf-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="890cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




