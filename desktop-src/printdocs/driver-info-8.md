---
description: Contient des informations sur le pilote d’imprimante.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Structure DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320613"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="50901-103">\_Structure info \_ 8 du pilote</span><span class="sxs-lookup"><span data-stu-id="50901-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="50901-104">Contient des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="50901-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="50901-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50901-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="50901-106">Membres</span><span class="sxs-lookup"><span data-stu-id="50901-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="50901-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="50901-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="50901-108">Version du système d’exploitation pour laquelle le pilote a été écrit.</span><span class="sxs-lookup"><span data-stu-id="50901-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="50901-109">La valeur prise en charge est 3.</span><span class="sxs-lookup"><span data-stu-id="50901-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="50901-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="50901-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="50901-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote (par exemple, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="50901-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="50901-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="50901-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="50901-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le pilote a été écrit (par exemple, Windows x86, Windows IA64 et Windows x64.</span><span class="sxs-lookup"><span data-stu-id="50901-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="50901-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="50901-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="50901-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient le pilote de périphérique (par exemple, C : \\ drivers \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="50901-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="50901-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="50901-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="50901-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier qui contient les données du pilote (par exemple, C : \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="50901-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="50901-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="50901-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="50901-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour la bibliothèque de liens dynamiques de configuration du pilote de périphérique (par exemple, C : \\ drivers \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="50901-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="50901-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="50901-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="50901-121">Pointeur vers une chaîne se terminant par un caractère null qui spécifie un nom de fichier ou un chemin d’accès complet et un nom de fichier pour le fichier d’aide du pilote de périphérique (par exemple, C : \\ drivers \\ PSCRPTUI. hlp).</span><span class="sxs-lookup"><span data-stu-id="50901-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="50901-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="50901-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="50901-123">Pointeur vers une mémoire tampon MultiSZ qui contient une séquence de chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="50901-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="50901-124">Chaque chaîne se terminant par un caractère NULL dans la mémoire tampon contient le nom d’un fichier dont le pilote dépend.</span><span class="sxs-lookup"><span data-stu-id="50901-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="50901-125">La séquence de chaînes se termine par une chaîne vide de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="50901-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="50901-126">Si **pDependentFiles** n’a pas la **valeur null** et qu’il ne contient aucun nom de fichier, il pointe vers une mémoire tampon qui contient deux chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="50901-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="50901-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="50901-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="50901-128">Pointeur vers une chaîne se terminant par un caractère null qui spécifie une analyse de langage (par exemple, « PJL Monitor »).</span><span class="sxs-lookup"><span data-stu-id="50901-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="50901-129">Ce membre peut être **null** et doit être spécifié uniquement pour les imprimantes capables d’effectuer une communication bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="50901-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="50901-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="50901-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="50901-131">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut du travail d’impression (par exemple, « EMF »).</span><span class="sxs-lookup"><span data-stu-id="50901-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="50901-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="50901-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="50901-133">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les noms de pilote d’imprimante antérieurs compatibles avec ce pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="50901-134">Par exemple, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="50901-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="50901-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="50901-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="50901-136">Date du package de pilotes, telle que codée dans les fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="50901-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="50901-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="50901-138">Numéro de version du pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-138">The version number of the driver.</span></span> <span data-ttu-id="50901-139">Cela provient de la structure de la version du pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="50901-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="50901-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="50901-141">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="50901-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="50901-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="50901-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="50901-143">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’URL du fabricant.</span><span class="sxs-lookup"><span data-stu-id="50901-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="50901-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="50901-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="50901-145">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’ID de matériel pour le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="50901-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="50901-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="50901-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="50901-147">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le fournisseur du pilote d’imprimante (par exemple, « Microsoft Windows 2000 »).</span><span class="sxs-lookup"><span data-stu-id="50901-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="50901-148">**pszPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="50901-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="50901-149">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le processeur d’impression (par exemple, « WinPrint »).</span><span class="sxs-lookup"><span data-stu-id="50901-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="50901-150">**pszVendorSetup**</span><span class="sxs-lookup"><span data-stu-id="50901-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="50901-151">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la DLL d’installation du pilote du fournisseur et le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="50901-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="50901-152">**pszzColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="50901-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="50901-153">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les profils de couleur associés au pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="50901-154">**pszInfPath**</span><span class="sxs-lookup"><span data-stu-id="50901-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="50901-155">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le chemin d’accès au fichier. inf du pilote dans le magasin de pilotes.</span><span class="sxs-lookup"><span data-stu-id="50901-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="50901-156">(Consultez la section Notes.) La valeur doit être **null** si les informations sur le pilote \_ \_ 8 sont passées à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="50901-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="50901-157">**dwPrinterDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="50901-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="50901-158">Indicateurs d’attribut pour les pilotes d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="50901-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="50901-159">La valeur doit être 0 si les informations sur le pilote \_ \_ 8 sont transmises à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="50901-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="50901-160">Dans le cas contraire, il peut s’agir de n’importe quelle combinaison des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="50901-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="50901-161">Nom/valeur de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="50901-161">Flag name/value</span></span>                                                         | <span data-ttu-id="50901-162">Signification</span><span class="sxs-lookup"><span data-stu-id="50901-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="50901-163">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="50901-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="50901-164">prise \_ en \_ charge des packages de pilotes d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="50901-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="50901-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="50901-165">0x00000001</span></span><br/>        | <span data-ttu-id="50901-166">Le pilote d’imprimante fait partie d’un package de pilotes.</span><span class="sxs-lookup"><span data-stu-id="50901-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="50901-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50901-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="50901-168">pilote d’imprimante \_ \_ XPS</span><span class="sxs-lookup"><span data-stu-id="50901-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="50901-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="50901-169">0x00000002</span></span><br/>                   | <span data-ttu-id="50901-170">Le pilote d’imprimante prend en charge le format Microsoft XPS décrit dans la [spécification XML Paper Specification](/previous-versions/windows/hardware/design/dn641615(v=vs.85))(en anglais), ainsi que dans le [comportement du produit, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="50901-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="50901-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-171">Windows 8</span></span><br/> <span data-ttu-id="50901-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-173">\_bac à \_ sable (sandbox) du pilote d’imprimante \_ activé</span><span class="sxs-lookup"><span data-stu-id="50901-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="50901-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="50901-174">0x00000004</span></span><br/>      | <span data-ttu-id="50901-175">Le pilote d’imprimante est compatible avec l' [isolement du pilote d’imprimante](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="50901-176">Pour plus d’informations, consultez [comportement du produit, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="50901-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="50901-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50901-177">Windows 7</span></span><br/> <span data-ttu-id="50901-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50901-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="50901-179">\_classe de pilote d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="50901-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="50901-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="50901-180">0x00000008</span></span><br/>                 | <span data-ttu-id="50901-181">Le pilote d’imprimante est un [pilote d’imprimante de classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="50901-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-182">Windows 8</span></span><br/> <span data-ttu-id="50901-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-184">pilote d’imprimante \_ \_ dérivé</span><span class="sxs-lookup"><span data-stu-id="50901-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="50901-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50901-185">0x00000010</span></span><br/>               | <span data-ttu-id="50901-186">Le pilote d’imprimante est un [pilote d’imprimante dérivé](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="50901-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-187">Windows 8</span></span><br/> <span data-ttu-id="50901-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-189">le \_ pilote d’imprimante \_ ne \_ partage pas</span><span class="sxs-lookup"><span data-stu-id="50901-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="50901-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="50901-190">0x00000020</span></span><br/>        | <span data-ttu-id="50901-191">Les imprimantes qui utilisent ce pilote d’imprimante ne peuvent pas être partagées.</span><span class="sxs-lookup"><span data-stu-id="50901-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="50901-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-192">Windows 8</span></span><br/> <span data-ttu-id="50901-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-194">\_ \_ télécopie catégorie du pilote d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="50901-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="50901-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="50901-195">0x00000040</span></span><br/>         | <span data-ttu-id="50901-196">Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de télécopie](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="50901-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-197">Windows 8</span></span><br/> <span data-ttu-id="50901-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-199">\_fichier de \_ catégorie du pilote d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="50901-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="50901-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="50901-200">0x00000080</span></span><br/>        | <span data-ttu-id="50901-201">Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de fichiers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="50901-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-202">Windows 8</span></span><br/> <span data-ttu-id="50901-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-204">catégorie de pilote d’imprimante \_ \_ \_ virtuelle</span><span class="sxs-lookup"><span data-stu-id="50901-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="50901-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="50901-205">0x00000100</span></span><br/>     | <span data-ttu-id="50901-206">Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes virtuelles](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="50901-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-207">Windows 8</span></span><br/> <span data-ttu-id="50901-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-209">\_service de \_ catégorie de pilote d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="50901-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="50901-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="50901-210">0x00000200</span></span><br/>     | <span data-ttu-id="50901-211">Le pilote d’imprimante est destiné à être utilisé avec les [imprimantes de service](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="50901-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="50901-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-212">Windows 8</span></span><br/> <span data-ttu-id="50901-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="50901-214">\_réinitialisation logicielle du pilote d’imprimante \_ \_ \_ requise</span><span class="sxs-lookup"><span data-stu-id="50901-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="50901-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="50901-215">0x00000400</span></span><br/> | <span data-ttu-id="50901-216">Les imprimantes qui utilisent ce pilote d’imprimante doivent suivre les instructions fournies dans la définition de la classe de périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="50901-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="50901-217">Pour plus d’informations, consultez [comportement du produit, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="50901-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="50901-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50901-218">Windows 8</span></span><br/> <span data-ttu-id="50901-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50901-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="50901-220">**pszzCoreDriverDependencies**</span><span class="sxs-lookup"><span data-stu-id="50901-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="50901-221">Pointeur vers une chaîne multiple se terminant par un caractère null qui spécifie tous les pilotes d’imprimante principaux dont dépend le pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="50901-222">La valeur doit être **null** si les informations sur le **pilote \_ \_ 8** sont passées à [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="50901-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="50901-223">**ftMinInboxDriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="50901-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="50901-224">La première date autorisée des pilotes fournis avec Windows et dont ce pilote dépend.</span><span class="sxs-lookup"><span data-stu-id="50901-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="50901-225">**dwlMinInboxDriverVerVersion**</span><span class="sxs-lookup"><span data-stu-id="50901-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="50901-226">La première version autorisée des pilotes fournis avec Windows et dont dépend ce pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50901-227">Notes</span><span class="sxs-lookup"><span data-stu-id="50901-227">Remarks</span></span>

<span data-ttu-id="50901-228">Les chaînes de ces membres sont contenues dans le fichier. inf qui est utilisé pour ajouter le pilote.</span><span class="sxs-lookup"><span data-stu-id="50901-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="50901-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50901-229">Requirements</span></span>



| <span data-ttu-id="50901-230">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50901-230">Requirement</span></span> | <span data-ttu-id="50901-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="50901-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50901-232">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50901-232">Minimum supported client</span></span><br/> | <span data-ttu-id="50901-233">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50901-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="50901-234">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50901-234">Minimum supported server</span></span><br/> | <span data-ttu-id="50901-235">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50901-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="50901-236">En-tête</span><span class="sxs-lookup"><span data-stu-id="50901-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="50901-237"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50901-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="50901-238">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="50901-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50901-239">**\_ \_ Informations sur \_ le pilote 8W** (Unicode) et **\_ \_ informations sur le pilote \_ 8A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="50901-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="50901-240">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50901-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50901-241">Impression</span><span class="sxs-lookup"><span data-stu-id="50901-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="50901-242">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="50901-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="50901-243">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="50901-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="50901-244">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="50901-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

