---
description: La \_ structure info \_ 5 du pilote contient des informations sur le pilote d’imprimante.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: Structure DRIVER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521386"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="513ae-103">\_Structure info \_ 5 du pilote</span><span class="sxs-lookup"><span data-stu-id="513ae-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="513ae-104">La **structure \_ info \_ 5 du pilote** contient des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="513ae-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="513ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="513ae-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="513ae-106">Membres</span><span class="sxs-lookup"><span data-stu-id="513ae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="513ae-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="513ae-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="513ae-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="513ae-109">La valeur prise en charge est 3.</span><span class="sxs-lookup"><span data-stu-id="513ae-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="513ae-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="513ae-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="513ae-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="513ae-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="513ae-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).</span><span class="sxs-lookup"><span data-stu-id="513ae-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="513ae-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="513ae-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, C : \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="513ae-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="513ae-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="513ae-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, C : \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="513ae-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="513ae-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="513ae-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de configuration du pilote de périphérique (par exemple, C : \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="513ae-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="513ae-120">**dwDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="513ae-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-121">Attributs du pilote, par exemple UMPD/KMPD.</span><span class="sxs-lookup"><span data-stu-id="513ae-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="513ae-122">**dwConfigVersion**</span><span class="sxs-lookup"><span data-stu-id="513ae-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-123">Nombre de fois où le fichier de configuration de ce pilote a été mis à niveau ou rétrogradé depuis le dernier redémarrage du spouleur.</span><span class="sxs-lookup"><span data-stu-id="513ae-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="513ae-124">**dwDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="513ae-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="513ae-125">Nombre de fois où le fichier de pilote de ce pilote a été mis à niveau ou rétrogradé depuis le dernier redémarrage du spouleur.</span><span class="sxs-lookup"><span data-stu-id="513ae-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="513ae-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="513ae-126">Requirements</span></span>



| <span data-ttu-id="513ae-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="513ae-127">Requirement</span></span> | <span data-ttu-id="513ae-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="513ae-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513ae-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="513ae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="513ae-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="513ae-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="513ae-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="513ae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="513ae-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="513ae-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="513ae-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="513ae-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="513ae-134"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="513ae-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="513ae-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="513ae-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="513ae-136">**\_ \_ Informations sur \_ le pilote 5W** (Unicode) et **\_ \_ informations sur le pilote \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="513ae-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="513ae-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="513ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513ae-138">Impression</span><span class="sxs-lookup"><span data-stu-id="513ae-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="513ae-139">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="513ae-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="513ae-140">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="513ae-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="513ae-141">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="513ae-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="513ae-142">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="513ae-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




