---
description: Cette classe est la classe de type d’événement pour les événements d’attente ALPC pour les nouveaux messages. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: Classe ALPC_Wait_For_New_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972239"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="ab98f-104">\_Attente ALPC \_ pour une \_ nouvelle classe de \_ message</span><span class="sxs-lookup"><span data-stu-id="ab98f-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="ab98f-105">Cette classe est la classe de type d’événement pour les événements d’attente ALPC pour les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="ab98f-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="ab98f-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="ab98f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab98f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab98f-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="ab98f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ab98f-108">Members</span></span>

<span data-ttu-id="ab98f-109">La classe d' **\_ attente ALPC pour le \_ \_ nouveau \_ message** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab98f-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="ab98f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab98f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab98f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab98f-111">Properties</span></span>

<span data-ttu-id="ab98f-112">La **classe \_ d’attente ALPC \_ pour les \_ nouveaux \_ messages** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ab98f-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab98f-113">**IsServerPort**</span><span class="sxs-lookup"><span data-stu-id="ab98f-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab98f-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab98f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab98f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab98f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab98f-116">Indique si le port est un port serveur.</span><span class="sxs-lookup"><span data-stu-id="ab98f-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="ab98f-117">**PortName**</span><span class="sxs-lookup"><span data-stu-id="ab98f-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab98f-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab98f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab98f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab98f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab98f-120">Chaîne qui contient le nom du port sur lequel ALPC est en attente.</span><span class="sxs-lookup"><span data-stu-id="ab98f-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab98f-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ab98f-121">Requirements</span></span>



| <span data-ttu-id="ab98f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab98f-122">Requirement</span></span> | <span data-ttu-id="ab98f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab98f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab98f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab98f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab98f-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab98f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab98f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab98f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab98f-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab98f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




