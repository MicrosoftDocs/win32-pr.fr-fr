---
description: La structure PROTOCOLINFO décrit un protocole.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: PROTOCOLINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521084"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="07791-103">PROTOCOLINFO, structure</span><span class="sxs-lookup"><span data-stu-id="07791-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="07791-104">La structure **PROTOCOLINFO** décrit un protocole.</span><span class="sxs-lookup"><span data-stu-id="07791-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="07791-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07791-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="07791-106">Membres</span><span class="sxs-lookup"><span data-stu-id="07791-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07791-107">**ProtocolID**</span><span class="sxs-lookup"><span data-stu-id="07791-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="07791-108">Identificateur de protocole attribué par le système de la session d’exécution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07791-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="07791-109">**Propriétédescription**</span><span class="sxs-lookup"><span data-stu-id="07791-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="07791-110">Base de données de propriétés du protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="07791-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="07791-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="07791-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="07791-112">Nom de protocole abrégé.</span><span class="sxs-lookup"><span data-stu-id="07791-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="07791-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="07791-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="07791-114">Nom de fichier d’aide facultatif associé au protocole.</span><span class="sxs-lookup"><span data-stu-id="07791-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="07791-115">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="07791-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="07791-116">Commentaire décrivant le protocole.</span><span class="sxs-lookup"><span data-stu-id="07791-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07791-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07791-117">Requirements</span></span>



| <span data-ttu-id="07791-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07791-118">Requirement</span></span> | <span data-ttu-id="07791-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="07791-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07791-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07791-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07791-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07791-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07791-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07791-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07791-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07791-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07791-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="07791-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="07791-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07791-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




