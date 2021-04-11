---
description: La \_ structure informations sur le pilote \_ 4 contient des informations sur le pilote d’imprimante.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Structure DRIVER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202694"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="a327a-103">\_Structure info \_ 4 du pilote</span><span class="sxs-lookup"><span data-stu-id="a327a-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="a327a-104">La **structure \_ informations \_ sur le pilote 4** contient des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="a327a-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a327a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a327a-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="a327a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a327a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a327a-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="a327a-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="a327a-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="a327a-109">La valeur prise en charge est 3.</span><span class="sxs-lookup"><span data-stu-id="a327a-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="a327a-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="a327a-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, « QMS 810 »).</span><span class="sxs-lookup"><span data-stu-id="a327a-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="a327a-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="a327a-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a327a-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="a327a-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="a327a-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier, un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, C : \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="a327a-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="a327a-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="a327a-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, C : \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="a327a-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="a327a-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="a327a-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de configuration du pilote de périphérique (par exemple, C : \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="a327a-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="a327a-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="a327a-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-121">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a327a-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="a327a-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="a327a-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-123">Pointeur vers une mémoire tampon MultiSZ qui contient une séquence de chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="a327a-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="a327a-124">Chaque chaîne se terminant par un caractère NULL dans la mémoire tampon contient le nom d’un fichier dont le pilote dépend.</span><span class="sxs-lookup"><span data-stu-id="a327a-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="a327a-125">La séquence de chaînes se termine par une chaîne vide de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="a327a-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="a327a-126">Si **pDependentFiles** n’a pas la **valeur null** et qu’il ne contient aucun nom de fichier, il pointe vers une mémoire tampon qui contient deux chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="a327a-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="a327a-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="a327a-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-128">Pointeur vers une chaîne se terminant par un caractère null qui spécifie une analyse de langage (par exemple, PJL Monitor).</span><span class="sxs-lookup"><span data-stu-id="a327a-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="a327a-129">Ce membre peut être **null** et doit être spécifié uniquement pour les imprimantes capables d’effectuer une communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="a327a-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="a327a-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="a327a-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-131">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut du travail d’impression (par exemple, EMF).</span><span class="sxs-lookup"><span data-stu-id="a327a-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="a327a-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="a327a-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="a327a-133">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les noms de pilote d’imprimante antérieurs compatibles avec ce pilote.</span><span class="sxs-lookup"><span data-stu-id="a327a-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="a327a-134">Par exemple, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="a327a-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a327a-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a327a-135">Requirements</span></span>



| <span data-ttu-id="a327a-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a327a-136">Requirement</span></span> | <span data-ttu-id="a327a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a327a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a327a-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a327a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a327a-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a327a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a327a-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a327a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a327a-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a327a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a327a-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="a327a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a327a-143"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a327a-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a327a-144">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a327a-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a327a-145">**\_ \_ Informations sur \_ le pilote 4W** (Unicode) et **\_ \_ informations sur le pilote \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a327a-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="a327a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a327a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a327a-147">Impression</span><span class="sxs-lookup"><span data-stu-id="a327a-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a327a-148">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a327a-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a327a-149">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a327a-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="a327a-150">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="a327a-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="a327a-151">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a327a-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




