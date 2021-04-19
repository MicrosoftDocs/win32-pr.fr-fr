---
description: Retourne l’offset d’un protocole spécifié dans le frame.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: GetProtocolStartOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544615"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="7400c-103">GetProtocolStartOffset fonction)</span><span class="sxs-lookup"><span data-stu-id="7400c-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="7400c-104">La fonction **GetProtocolStartOffset** retourne le décalage d’un protocole spécifié dans le frame.</span><span class="sxs-lookup"><span data-stu-id="7400c-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7400c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7400c-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="7400c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7400c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7400c-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="7400c-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="7400c-108">Handle du frame.</span><span class="sxs-lookup"><span data-stu-id="7400c-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="7400c-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="7400c-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="7400c-110">Nom de protocole, tel que TCP.</span><span class="sxs-lookup"><span data-stu-id="7400c-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7400c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7400c-111">Return value</span></span>

<span data-ttu-id="7400c-112">Si la fonction réussit, la valeur de retour est un décalage **DWORD** au début du protocole dans lequel la recherche d’une valeur de retour égale à zéro indique que le protocole est le premier protocole dans le frame.</span><span class="sxs-lookup"><span data-stu-id="7400c-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="7400c-113">Si la fonction échoue, le protocole n’est pas dans le frame, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="7400c-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7400c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7400c-114">Remarks</span></span>

<span data-ttu-id="7400c-115">Quand le handle d’un frame est donné, cette fonction retourne l’offset à un protocole spécifié dans le frame.</span><span class="sxs-lookup"><span data-stu-id="7400c-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="7400c-116">Par exemple, pour déterminer si le cadre est un frame DNS, l’analyseur DNS requiert l’adresse du port du protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="7400c-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="7400c-117">L’analyseur DNS appelle cette fonction avec TCP comme valeur *ProtocolName* .</span><span class="sxs-lookup"><span data-stu-id="7400c-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="7400c-118">Si le frame est reconnu par le protocole TCP, le **mot** offset à partir du début du frame jusqu’au début de la trame TCP est retourné.</span><span class="sxs-lookup"><span data-stu-id="7400c-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="7400c-119">S’il n’existe aucun protocole TCP, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="7400c-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="7400c-120">Cette fonction recherche le début d’un protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="7400c-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="7400c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7400c-121">Requirements</span></span>



| <span data-ttu-id="7400c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7400c-122">Requirement</span></span> | <span data-ttu-id="7400c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7400c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7400c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7400c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7400c-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7400c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7400c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7400c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7400c-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7400c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7400c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7400c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7400c-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7400c-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7400c-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7400c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7400c-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7400c-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7400c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7400c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7400c-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7400c-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




