---
description: La \_ structure HANDOFFENTRY de PF définit un protocole qui Moniteur réseau ajoute au jeu de remise d’un analyseur.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Structure de PF_HANDOFFENTRY (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541861"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="7ddc4-103">PF \_ HANDOFFENTRY, structure</span><span class="sxs-lookup"><span data-stu-id="7ddc4-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="7ddc4-104">La **structure \_ HANDOFFENTRY de PF** définit un protocole qui Moniteur réseau ajoute au jeu de remise d’un analyseur.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ddc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ddc4-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="7ddc4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7ddc4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ddc4-107">**szIniFile**</span><span class="sxs-lookup"><span data-stu-id="7ddc4-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="7ddc4-108">Nom du fichier INI associé au protocole.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7ddc4-109">**szIniSection**</span><span class="sxs-lookup"><span data-stu-id="7ddc4-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="7ddc4-110">Étiquette de section dans le fichier INI.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="7ddc4-111">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="7ddc4-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="7ddc4-112">Nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7ddc4-113">**dwHandOffValue**</span><span class="sxs-lookup"><span data-stu-id="7ddc4-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="7ddc4-114">Valeur associée au protocole.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7ddc4-115">**ValueFormatBase**</span><span class="sxs-lookup"><span data-stu-id="7ddc4-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="7ddc4-116">Base numérique de la valeur de protocole spécifiée dans **dwHandOffValue**.</span><span class="sxs-lookup"><span data-stu-id="7ddc4-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="7ddc4-117">La fonction **ValueFormatBase** doit être définie sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7ddc4-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="7ddc4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ddc4-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="7ddc4-119">Signification</span><span class="sxs-lookup"><span data-stu-id="7ddc4-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="7ddc4-120"><dt>**BASE de format de valeur de transfert \_ \_ \_ \_ inconnue**</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc4-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="7ddc4-121">Base inconnue</span><span class="sxs-lookup"><span data-stu-id="7ddc4-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="7ddc4-122"><dt>**FORMAT de la valeur de transfert \_ \_ \_ décimal de base \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc4-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="7ddc4-123">Base décimale</span><span class="sxs-lookup"><span data-stu-id="7ddc4-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="7ddc4-124"><dt>**\_hexadécimal de \_ base de format de valeur de transfert \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc4-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="7ddc4-125">Base hexadécimale</span><span class="sxs-lookup"><span data-stu-id="7ddc4-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ddc4-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7ddc4-126">Remarks</span></span>

<span data-ttu-id="7ddc4-127">Un tableau des structures **\_ HANDOFFENTRY PF** est utilisé dans la structure [ \_ HANDOFFSET de PF](pf-handoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddc4-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ddc4-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ddc4-128">Requirements</span></span>



| <span data-ttu-id="7ddc4-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ddc4-129">Requirement</span></span> | <span data-ttu-id="7ddc4-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ddc4-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddc4-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ddc4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddc4-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ddc4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7ddc4-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ddc4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddc4-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ddc4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7ddc4-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ddc4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddc4-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddc4-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ddc4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ddc4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddc4-138">\_HANDOFFSET PF</span><span class="sxs-lookup"><span data-stu-id="7ddc4-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




