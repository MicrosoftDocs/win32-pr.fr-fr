---
description: La \_ structure des \_ valeurs d’énumération d’imprimante spécifie le nom, le type et les données de la valeur pour une valeur de configuration d’imprimante retournée par la fonction EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Structure PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541837"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="9a723-103">\_Structure des valeurs d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9a723-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="9a723-104">La structure des **\_ \_ valeurs d’énumération d’imprimante** spécifie le nom, le type et les données de la valeur pour une valeur de configuration d’imprimante retournée par la fonction [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="9a723-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a723-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a723-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="9a723-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9a723-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a723-107">**pValueName**</span><span class="sxs-lookup"><span data-stu-id="9a723-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="9a723-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="9a723-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="9a723-109">**cbValueName**</span><span class="sxs-lookup"><span data-stu-id="9a723-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="9a723-110">Nombre d’octets dans le membre **pValueName** , y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="9a723-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="9a723-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="9a723-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="9a723-112">Code indiquant le type de données vers lequel pointe le membre **pData** .</span><span class="sxs-lookup"><span data-stu-id="9a723-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="9a723-113">Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="9a723-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="9a723-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="9a723-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="9a723-115">Pointeur vers une mémoire tampon contenant les données de la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="9a723-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="9a723-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9a723-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="9a723-117">Nombre d’octets récupérés dans la mémoire tampon **pData** .</span><span class="sxs-lookup"><span data-stu-id="9a723-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a723-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a723-118">Requirements</span></span>



| <span data-ttu-id="9a723-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a723-119">Requirement</span></span> | <span data-ttu-id="9a723-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a723-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a723-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a723-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a723-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a723-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a723-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a723-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a723-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a723-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a723-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a723-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a723-126"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a723-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9a723-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9a723-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9a723-128">**\_ \_ \_ VALUESW d’énumération d’imprimante** (Unicode) et **\_ \_ \_ valeurs d’énumération d’imprimante** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9a723-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9a723-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a723-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a723-130">Impression</span><span class="sxs-lookup"><span data-stu-id="9a723-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9a723-131">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="9a723-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9a723-132">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="9a723-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

