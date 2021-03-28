---
description: Cette classe est la classe de type d’événement pour les événements de message d’envoi ALPC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Classe ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113891"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="b37f2-104">Classe de message d' \_ envoi ALPC \_</span><span class="sxs-lookup"><span data-stu-id="b37f2-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="b37f2-105">Cette classe est la classe de type d’événement pour les événements de message d’envoi ALPC.</span><span class="sxs-lookup"><span data-stu-id="b37f2-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="b37f2-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="b37f2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b37f2-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="b37f2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b37f2-108">Members</span></span>

<span data-ttu-id="b37f2-109">La classe de **\_ \_ message d’envoi ALPC** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b37f2-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="b37f2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b37f2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b37f2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b37f2-111">Properties</span></span>

<span data-ttu-id="b37f2-112">La classe de **\_ \_ message d’envoi ALPC** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b37f2-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b37f2-113">**ID**</span><span class="sxs-lookup"><span data-stu-id="b37f2-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37f2-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b37f2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37f2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b37f2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b37f2-116">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="b37f2-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b37f2-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b37f2-117">Requirements</span></span>



| <span data-ttu-id="b37f2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b37f2-118">Requirement</span></span> | <span data-ttu-id="b37f2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b37f2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b37f2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b37f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b37f2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b37f2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b37f2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b37f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b37f2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b37f2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




