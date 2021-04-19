---
description: La \_ structure par défaut de l’imprimante spécifie le type de données par défaut, l’environnement, les données d’initialisation et les droits d’accès d’une imprimante.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Structure PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534333"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="74800-103">\_Structure par défaut de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="74800-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="74800-104">La **structure \_ par défaut** de l’imprimante spécifie le type de données par défaut, l’environnement, les données d’initialisation et les droits d’accès d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="74800-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="74800-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74800-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="74800-106">Membres</span><span class="sxs-lookup"><span data-stu-id="74800-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="74800-107">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="74800-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="74800-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="74800-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="74800-109">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="74800-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="74800-110">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui identifie l’environnement par défaut et les données d’initialisation d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="74800-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="74800-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="74800-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="74800-112">Spécifie les droits d’accès souhaités pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="74800-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="74800-113">La fonction [**OpenPrinter**](openprinter.md) utilise ce membre pour définir les droits d’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="74800-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="74800-114">Ces droits peuvent affecter le fonctionnement des fonctions [**SetPrinter**](setprinter.md) et [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="74800-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="74800-115">Les droits d’accès peuvent être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="74800-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="74800-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="74800-116">Value</span></span>                                       | <span data-ttu-id="74800-117">Signification</span><span class="sxs-lookup"><span data-stu-id="74800-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74800-118">\_administration de l’accès aux imprimantes \_</span><span class="sxs-lookup"><span data-stu-id="74800-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="74800-119">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="74800-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="74800-120">\_utilisation de l’accès à l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="74800-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="74800-121">Pour effectuer des opérations d’impression de base.</span><span class="sxs-lookup"><span data-stu-id="74800-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="74800-122">\_gestion de l’accès à l’imprimante \_ \_ limitée</span><span class="sxs-lookup"><span data-stu-id="74800-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="74800-123">Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="74800-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="74800-124">Cette valeur est disponible à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="74800-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="74800-125">\_tout \_ accès imprimante</span><span class="sxs-lookup"><span data-stu-id="74800-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="74800-126">Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de la synchronisation (voir [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="74800-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="74800-127">valeurs de sécurité génériques, telles que WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="74800-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="74800-128">Pour autoriser des droits d’accès de contrôle spécifiques.</span><span class="sxs-lookup"><span data-stu-id="74800-128">To allow specific control access rights.</span></span> <span data-ttu-id="74800-129">Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="74800-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74800-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74800-130">Requirements</span></span>



| <span data-ttu-id="74800-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74800-131">Requirement</span></span> | <span data-ttu-id="74800-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="74800-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74800-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74800-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74800-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74800-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74800-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74800-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74800-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74800-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74800-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="74800-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="74800-138"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74800-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74800-139">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="74800-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74800-140">**\_ \_ DEFAULTSW d’imprimante** (Unicode) et **\_ \_ Erreurs d’imprimante** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74800-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="74800-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74800-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74800-142">Impression</span><span class="sxs-lookup"><span data-stu-id="74800-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74800-143">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="74800-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="74800-144">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="74800-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="74800-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="74800-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="74800-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="74800-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="74800-147">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="74800-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

