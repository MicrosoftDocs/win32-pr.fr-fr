---
description: La \_ structure d’informations sur le port \_ 2 identifie un port d’imprimante pris en charge.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Structure PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520024"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="fdee0-103">\_Structure des informations sur le port \_ 2</span><span class="sxs-lookup"><span data-stu-id="fdee0-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="fdee0-104">La structure d' **\_ informations sur le port \_ 2** identifie un port d’imprimante pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fdee0-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdee0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdee0-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="fdee0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fdee0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fdee0-107">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="fdee0-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="fdee0-108">Pointeur vers une chaîne se terminant par un caractère null qui identifie un port imprimante pris en charge (par exemple, « LPT1 : »).</span><span class="sxs-lookup"><span data-stu-id="fdee0-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="fdee0-109">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="fdee0-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="fdee0-110">Pointeur vers une chaîne se terminant par un caractère null qui identifie une analyse installée (par exemple, « PJL Monitor »).</span><span class="sxs-lookup"><span data-stu-id="fdee0-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="fdee0-111">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="fdee0-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fdee0-112">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="fdee0-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="fdee0-113">Pointeur vers une chaîne se terminant par un caractère null qui décrit le port plus en détail (par exemple, si **pPortName** est « LPT1 : », **pDescription** est « port imprimante »).</span><span class="sxs-lookup"><span data-stu-id="fdee0-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="fdee0-114">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="fdee0-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fdee0-115">**fPortType**</span><span class="sxs-lookup"><span data-stu-id="fdee0-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="fdee0-116">Masque de masque décrivant le type de port.</span><span class="sxs-lookup"><span data-stu-id="fdee0-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="fdee0-117">Ce membre peut être une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="fdee0-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="fdee0-118">**\_écriture du type de port \_**</span><span class="sxs-lookup"><span data-stu-id="fdee0-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="fdee0-119">**TYPE de PORT \_ \_ lu**</span><span class="sxs-lookup"><span data-stu-id="fdee0-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="fdee0-120">**TYPE de PORT \_ \_ Redirigé**</span><span class="sxs-lookup"><span data-stu-id="fdee0-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="fdee0-121">**TYPE de PORT \_ \_ NET \_ attaché**</span><span class="sxs-lookup"><span data-stu-id="fdee0-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fdee0-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fdee0-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fdee0-123">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fdee0-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdee0-124">Notes</span><span class="sxs-lookup"><span data-stu-id="fdee0-124">Remarks</span></span>

<span data-ttu-id="fdee0-125">Utilisez la **structure \_ informations \_ sur le port 2** lors de l’appel de [**EnumPorts**](enumports.md) si plusieurs moniteurs prennent en charge les mêmes ports.</span><span class="sxs-lookup"><span data-stu-id="fdee0-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="fdee0-126">Le membre **fPortType** peut être interrogé pour déterminer les informations relatives au port.</span><span class="sxs-lookup"><span data-stu-id="fdee0-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="fdee0-127">Notez que les paramètres de port n’affectent pas les attributs d’imprimante (tels qu’ils sont retournés par le membre **attributs** de [**Printer \_ info \_ 2**](printer-info-2.md)).</span><span class="sxs-lookup"><span data-stu-id="fdee0-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdee0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdee0-128">Requirements</span></span>



| <span data-ttu-id="fdee0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdee0-129">Requirement</span></span> | <span data-ttu-id="fdee0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdee0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdee0-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdee0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fdee0-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdee0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fdee0-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdee0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fdee0-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdee0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fdee0-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdee0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdee0-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdee0-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fdee0-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fdee0-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fdee0-138">**\_ \_ Informations sur \_ le port 2S** (Unicode) et **\_ \_ informations sur le port \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fdee0-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="fdee0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdee0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdee0-140">Impression</span><span class="sxs-lookup"><span data-stu-id="fdee0-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fdee0-141">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="fdee0-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fdee0-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="fdee0-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




