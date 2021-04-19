---
description: La \_ structure informations sur le pilote \_ 6 contient des informations sur le pilote d’imprimante.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Structure DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529160"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="ca88f-103">\_Structure info \_ 6 du pilote</span><span class="sxs-lookup"><span data-stu-id="ca88f-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="ca88f-104">La **structure \_ informations \_ sur le pilote 6** contient des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ca88f-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca88f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca88f-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="ca88f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ca88f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca88f-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="ca88f-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="ca88f-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="ca88f-109">La valeur prise en charge est 3.</span><span class="sxs-lookup"><span data-stu-id="ca88f-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="ca88f-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="ca88f-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ca88f-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows NT x86, Windows IA64 et Windows x64.</span><span class="sxs-lookup"><span data-stu-id="ca88f-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="ca88f-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, C : \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="ca88f-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="ca88f-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, C : \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="ca88f-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="ca88f-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de configuration du pilote de périphérique (par exemple, C : \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="ca88f-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="ca88f-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-121">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique (par exemple, C : \\ drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="ca88f-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="ca88f-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-123">Pointeur vers une mémoire tampon MultiSZ qui contient une séquence de chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="ca88f-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="ca88f-124">Chaque chaîne se terminant par un caractère NULL dans la mémoire tampon contient le nom d’un fichier dont le pilote dépend.</span><span class="sxs-lookup"><span data-stu-id="ca88f-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="ca88f-125">La séquence de chaînes se termine par une chaîne vide de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="ca88f-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="ca88f-126">Si **pDependentFiles** n’a pas la **valeur null** et qu’il ne contient aucun nom de fichier, il pointe vers une mémoire tampon qui contient deux chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="ca88f-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="ca88f-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-128">Pointeur vers une chaîne se terminant par un caractère null qui spécifie une analyse de langage (par exemple, « PJL Monitor »).</span><span class="sxs-lookup"><span data-stu-id="ca88f-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="ca88f-129">Ce membre peut être **null** et doit être spécifié uniquement pour les imprimantes capables d’effectuer une communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="ca88f-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="ca88f-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-131">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut du travail d’impression (par exemple, « EMF »).</span><span class="sxs-lookup"><span data-stu-id="ca88f-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="ca88f-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-133">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les noms de pilote d’imprimante antérieurs compatibles avec ce pilote.</span><span class="sxs-lookup"><span data-stu-id="ca88f-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="ca88f-134">Par exemple, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="ca88f-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="ca88f-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-136">Date du package de pilotes, telle que codée dans les fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="ca88f-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="ca88f-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-138">Numéro de version du pilote.</span><span class="sxs-lookup"><span data-stu-id="ca88f-138">Version number of the driver.</span></span> <span data-ttu-id="ca88f-139">Cela provient de la structure de version du pilote.</span><span class="sxs-lookup"><span data-stu-id="ca88f-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="ca88f-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-141">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="ca88f-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="ca88f-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-143">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’URL du fabricant.</span><span class="sxs-lookup"><span data-stu-id="ca88f-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="ca88f-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-145">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’ID de matériel pour le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ca88f-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="ca88f-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="ca88f-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="ca88f-147">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le fournisseur du pilote d’imprimante (par exemple, « Microsoft Windows 2000 »)</span><span class="sxs-lookup"><span data-stu-id="ca88f-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca88f-148">Notes</span><span class="sxs-lookup"><span data-stu-id="ca88f-148">Remarks</span></span>

<span data-ttu-id="ca88f-149">Les chaînes de ces membres sont contenues dans le fichier. inf qui est utilisé pour ajouter le pilote.</span><span class="sxs-lookup"><span data-stu-id="ca88f-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="ca88f-150">Si vous appelez [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md) avec un *niveau* non égal à 6, puis que vous appelez [**GetPrinterDriver**](getprinterdriver.md) ou [**EnumPrinterDrivers**](enumprinterdrivers.md) avec un *niveau* égal à 6, la structure **\_ informations sur le pilote \_ 6** est retournée avec **pszMfgName**, **pszOEMUrl**, **pszHardwareID** et **pszProvider** défini sur **null**, **dwlDriverVersion** défini sur 0 et **ftDriverDate** défini sur (0,0).</span><span class="sxs-lookup"><span data-stu-id="ca88f-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca88f-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca88f-151">Requirements</span></span>



| <span data-ttu-id="ca88f-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca88f-152">Requirement</span></span> | <span data-ttu-id="ca88f-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca88f-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca88f-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca88f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ca88f-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca88f-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca88f-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca88f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ca88f-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca88f-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca88f-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca88f-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca88f-159"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca88f-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ca88f-160">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ca88f-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca88f-161">**\_ \_ Informations sur \_ le pilote 6W** (Unicode) et **\_ \_ informations sur \_ le pilote** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca88f-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ca88f-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca88f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca88f-163">Impression</span><span class="sxs-lookup"><span data-stu-id="ca88f-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ca88f-164">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ca88f-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ca88f-165">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ca88f-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ca88f-166">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="ca88f-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="ca88f-167">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ca88f-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ca88f-168">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ca88f-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




