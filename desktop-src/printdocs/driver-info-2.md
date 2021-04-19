---
description: La \_ structure informations sur le pilote \_ 2 identifie un pilote d’imprimante, le numéro de version du pilote, l’environnement pour lequel le pilote a été écrit, le nom du fichier dans lequel le pilote est stocké, et ainsi de suite.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Structure DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517690"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="c1280-103">\_Structure informations sur le pilote \_ 2</span><span class="sxs-lookup"><span data-stu-id="c1280-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="c1280-104">La **structure \_ informations \_ sur le pilote 2** identifie un pilote d’imprimante, le numéro de version du pilote, l’environnement pour lequel le pilote a été écrit, le nom du fichier dans lequel le pilote est stocké, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c1280-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1280-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1280-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="c1280-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c1280-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1280-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="c1280-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="c1280-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="c1280-109">La valeur prise en charge est 3.</span><span class="sxs-lookup"><span data-stu-id="c1280-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="c1280-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="c1280-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, « QMS 810 »).</span><span class="sxs-lookup"><span data-stu-id="c1280-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="c1280-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="c1280-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64).</span><span class="sxs-lookup"><span data-stu-id="c1280-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="c1280-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="c1280-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, « c : \\ drivers \\pscript.dll »).</span><span class="sxs-lookup"><span data-stu-id="c1280-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="c1280-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="c1280-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, « c : \\ drivers \\ Qms810. PPD »).</span><span class="sxs-lookup"><span data-stu-id="c1280-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="c1280-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="c1280-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="c1280-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la configuration. dll du pilote de l’appareil (par exemple, « c : \\ drivers \\Pscrptui.dll »).</span><span class="sxs-lookup"><span data-stu-id="c1280-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1280-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1280-120">Requirements</span></span>



| <span data-ttu-id="c1280-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1280-121">Requirement</span></span> | <span data-ttu-id="c1280-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1280-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1280-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1280-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1280-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1280-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1280-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1280-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1280-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1280-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1280-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1280-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1280-128"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1280-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c1280-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c1280-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1280-130">**\_ \_ Informations sur \_ le pilote 2S** (Unicode) et **\_ \_ informations sur le pilote \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c1280-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="c1280-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1280-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1280-132">Impression</span><span class="sxs-lookup"><span data-stu-id="c1280-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c1280-133">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c1280-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c1280-134">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c1280-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="c1280-135">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c1280-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




