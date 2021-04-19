---
description: La \_ structure informations sur le pilote \_ 3 contient des informations sur le pilote d’imprimante.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Structure DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529395"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="42882-103">\_Structure info du pilote \_ 3</span><span class="sxs-lookup"><span data-stu-id="42882-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="42882-104">La **structure \_ informations \_ sur le pilote 3** contient des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="42882-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="42882-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42882-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="42882-106">Membres</span><span class="sxs-lookup"><span data-stu-id="42882-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="42882-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="42882-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="42882-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="42882-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="42882-109">Les valeurs prises en charge sont 3 et 4, qui représentent respectivement les pilotes v3 et v4.</span><span class="sxs-lookup"><span data-stu-id="42882-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="42882-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="42882-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="42882-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, « QMS 810 »).</span><span class="sxs-lookup"><span data-stu-id="42882-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="42882-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="42882-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="42882-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).</span><span class="sxs-lookup"><span data-stu-id="42882-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="42882-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="42882-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="42882-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, « C : \\ drivers \\Pscript.dll »).</span><span class="sxs-lookup"><span data-stu-id="42882-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="42882-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="42882-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="42882-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, « C : \\ drivers \\ Qms810. PPD »).</span><span class="sxs-lookup"><span data-stu-id="42882-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="42882-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="42882-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="42882-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de la configuration du pilote de périphérique (par exemple, « C : \\ drivers \\Pscrptui.dll »).</span><span class="sxs-lookup"><span data-stu-id="42882-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="42882-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="42882-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="42882-121">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="42882-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="42882-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="42882-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="42882-123">Pointeur vers une mémoire tampon MultiSZ qui contient une séquence de chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="42882-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="42882-124">Chaque chaîne se terminant par un caractère NULL dans la mémoire tampon contient le nom d’un fichier dont le pilote dépend.</span><span class="sxs-lookup"><span data-stu-id="42882-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="42882-125">La séquence de chaînes se termine par une chaîne vide de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="42882-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="42882-126">Si **pDependentFiles** n’a pas la **valeur null** et qu’il ne contient aucun nom de fichier, il pointe vers une mémoire tampon qui contient deux chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="42882-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="42882-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="42882-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="42882-128">Pointeur vers une chaîne se terminant par un caractère null qui spécifie une analyse de langage (par exemple, « PJL Monitor »).</span><span class="sxs-lookup"><span data-stu-id="42882-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="42882-129">Ce membre peut être **null** et doit être spécifié uniquement pour les imprimantes capables d’effectuer une communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="42882-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="42882-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="42882-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="42882-131">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut du travail d’impression (par exemple, « EMF »).</span><span class="sxs-lookup"><span data-stu-id="42882-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42882-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42882-132">Requirements</span></span>



| <span data-ttu-id="42882-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42882-133">Requirement</span></span> | <span data-ttu-id="42882-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="42882-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42882-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42882-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42882-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42882-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="42882-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42882-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42882-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42882-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="42882-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="42882-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="42882-140"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42882-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="42882-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="42882-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="42882-142">**\_ \_ Informations sur \_ le pilote 3W** (Unicode) et **\_ \_ informations sur le pilote \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="42882-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="42882-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42882-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42882-144">Impression</span><span class="sxs-lookup"><span data-stu-id="42882-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="42882-145">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="42882-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="42882-146">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="42882-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="42882-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="42882-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="42882-148">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="42882-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




