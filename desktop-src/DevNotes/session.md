---
description: La structure de la SESSION contient des informations sur la session active.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Structure de SESSION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747669"
---
# <a name="session-structure"></a><span data-ttu-id="3cacc-103">Structure de SESSION</span><span class="sxs-lookup"><span data-stu-id="3cacc-103">SESSION structure</span></span>

<span data-ttu-id="3cacc-104">\[Cette structure contient des informations requises uniquement lorsque vous utilisez les fonctions **DeleteExtractedFiles** et **extract** , qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3cacc-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="3cacc-105">Cette documentation est fournie à titre d’information uniquement.\]</span><span class="sxs-lookup"><span data-stu-id="3cacc-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="3cacc-106">La structure de la **session** contient des informations sur la session active.</span><span class="sxs-lookup"><span data-stu-id="3cacc-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cacc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cacc-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="3cacc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3cacc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3cacc-109">**agir**</span><span class="sxs-lookup"><span data-stu-id="3cacc-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-110">l’action à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3cacc-110">The action to perform.</span></span> <span data-ttu-id="3cacc-111">Ce membre peut être l’une des valeurs du type énuméré suivant.</span><span class="sxs-lookup"><span data-stu-id="3cacc-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="3cacc-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="3cacc-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-113">Handle d’une liste de fichiers spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3cacc-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="3cacc-114">Ce type de données est déclaré comme suit :</span><span class="sxs-lookup"><span data-stu-id="3cacc-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="3cacc-115">**fAllCabinets**</span><span class="sxs-lookup"><span data-stu-id="3cacc-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-116">Indicateur qui signale si plusieurs fichiers CAB doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="3cacc-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="3cacc-117">Si cette valeur est **true**, les armoires de continuation sont traitées.</span><span class="sxs-lookup"><span data-stu-id="3cacc-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-118">**fOverwrite**</span><span class="sxs-lookup"><span data-stu-id="3cacc-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-119">Indicateur qui signale si les fichiers existants doivent être remplacés.</span><span class="sxs-lookup"><span data-stu-id="3cacc-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="3cacc-120">Si cette valeur est **true**, les fichiers existants sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="3cacc-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-121">**fNoLineFeed**</span><span class="sxs-lookup"><span data-stu-id="3cacc-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-122">Indicateur qui signale si le dernier `printf` appel a les caractères de saut de ligne ( `\n` ).</span><span class="sxs-lookup"><span data-stu-id="3cacc-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="3cacc-123">Si cette valeur est **true**, le dernier `printf` appel n’a pas inclus les caractères de saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="3cacc-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-124">**fSelfExtract**</span><span class="sxs-lookup"><span data-stu-id="3cacc-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-125">Indicateur qui indique si un fichier cab est auto-extractible.</span><span class="sxs-lookup"><span data-stu-id="3cacc-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="3cacc-126">Si cette valeur est **true**, l’armoire est auto-extractible.</span><span class="sxs-lookup"><span data-stu-id="3cacc-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-127">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="3cacc-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-128">Longueur de la partie exécutable (. exe) d’un fichier cab à extraction automatique.</span><span class="sxs-lookup"><span data-stu-id="3cacc-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-129">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="3cacc-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-130">Longueur de la partie du fichier CAB d’un fichier cab à extraction automatique.</span><span class="sxs-lookup"><span data-stu-id="3cacc-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-131">**ahfSelf**</span><span class="sxs-lookup"><span data-stu-id="3cacc-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-132">Descripteurs de fichiers dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="3cacc-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="3cacc-133">**cErrors**</span><span class="sxs-lookup"><span data-stu-id="3cacc-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-134">Nombre d’erreurs rencontrées pendant la session d’extraction.</span><span class="sxs-lookup"><span data-stu-id="3cacc-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="3cacc-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-136">Handle vers le contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="3cacc-136">A handle to the FDI context.</span></span> <span data-ttu-id="3cacc-137">Ce type de données est déclaré comme suit :</span><span class="sxs-lookup"><span data-stu-id="3cacc-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="3cacc-138">**ERF**</span><span class="sxs-lookup"><span data-stu-id="3cacc-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-139">Structure d’erreur FDI.</span><span class="sxs-lookup"><span data-stu-id="3cacc-139">The FDI error structure.</span></span> <span data-ttu-id="3cacc-140">Consultez [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="3cacc-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-141">**cFiles**</span><span class="sxs-lookup"><span data-stu-id="3cacc-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-142">Nombre de fichiers traités.</span><span class="sxs-lookup"><span data-stu-id="3cacc-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-143">**cbTotalBytes**</span><span class="sxs-lookup"><span data-stu-id="3cacc-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-144">Nombre total d’octets extraits.</span><span class="sxs-lookup"><span data-stu-id="3cacc-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-145">**perr**</span><span class="sxs-lookup"><span data-stu-id="3cacc-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-146">L’étape FDI.</span><span class="sxs-lookup"><span data-stu-id="3cacc-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-147">**ateliers**</span><span class="sxs-lookup"><span data-stu-id="3cacc-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-148">Erreur du fichier de débordement.</span><span class="sxs-lookup"><span data-stu-id="3cacc-148">The spill file error.</span></span> <span data-ttu-id="3cacc-149">Ce membre peut être l’une des valeurs du type énuméré suivant.</span><span class="sxs-lookup"><span data-stu-id="3cacc-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="3cacc-150">**cbSpill**</span><span class="sxs-lookup"><span data-stu-id="3cacc-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-151">Taille du fichier de débordement demandé.</span><span class="sxs-lookup"><span data-stu-id="3cacc-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-152">**achSelf**</span><span class="sxs-lookup"><span data-stu-id="3cacc-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-153">Nom du fichier exécutable (. exe).</span><span class="sxs-lookup"><span data-stu-id="3cacc-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="3cacc-154">**achMsg**</span><span class="sxs-lookup"><span data-stu-id="3cacc-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-155">Mémoire tampon de mise en forme du message.</span><span class="sxs-lookup"><span data-stu-id="3cacc-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="3cacc-156">**achLine**</span><span class="sxs-lookup"><span data-stu-id="3cacc-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-157">Mémoire tampon de mise en forme de ligne.</span><span class="sxs-lookup"><span data-stu-id="3cacc-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-158">**achLocation**</span><span class="sxs-lookup"><span data-stu-id="3cacc-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-159">Répertoire de sortie.</span><span class="sxs-lookup"><span data-stu-id="3cacc-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-160">**achFile**</span><span class="sxs-lookup"><span data-stu-id="3cacc-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-161">Nom de fichier actuel en cours d’extraction.</span><span class="sxs-lookup"><span data-stu-id="3cacc-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-162">**achDest**</span><span class="sxs-lookup"><span data-stu-id="3cacc-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-163">Nom du fichier de destination forcé.</span><span class="sxs-lookup"><span data-stu-id="3cacc-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-164">**achCabPath**</span><span class="sxs-lookup"><span data-stu-id="3cacc-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-165">Chemin d’accès à examiner pour un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="3cacc-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-166">**fContinuationCabinet**</span><span class="sxs-lookup"><span data-stu-id="3cacc-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-167">Indicateur qui signale si le fichier CAB actuel est le premier traité.</span><span class="sxs-lookup"><span data-stu-id="3cacc-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="3cacc-168">Si la valeur est **true**, le premier fichier CAB n’est pas traité.</span><span class="sxs-lookup"><span data-stu-id="3cacc-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-169">**fShowReserveInfo**</span><span class="sxs-lookup"><span data-stu-id="3cacc-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-170">Indicateur qui spécifie si les informations de réserve doivent être fournies.</span><span class="sxs-lookup"><span data-stu-id="3cacc-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="3cacc-171">Si la valeur est **true**, les informations sont rendues disponibles.</span><span class="sxs-lookup"><span data-stu-id="3cacc-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-172">**fNextCabCalled**</span><span class="sxs-lookup"><span data-stu-id="3cacc-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-173">Ce membre fournit un moyen de déterminer les entrées **ACAB** à utiliser si nous traitons tous les fichiers d’un jeu de fichiers CAB (**fAllCabinet** a la valeur **true**).</span><span class="sxs-lookup"><span data-stu-id="3cacc-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-174">**acab**</span><span class="sxs-lookup"><span data-stu-id="3cacc-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-175">Les deux dernières entrées dans le jeu de fichiers CAB.</span><span class="sxs-lookup"><span data-stu-id="3cacc-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="3cacc-176">Cette structure est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="3cacc-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="3cacc-177">**achZap**</span><span class="sxs-lookup"><span data-stu-id="3cacc-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-178">Préfixe à supprimer du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3cacc-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="3cacc-179">**achCabinetFile**</span><span class="sxs-lookup"><span data-stu-id="3cacc-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-180">Fichier CAB actuel.</span><span class="sxs-lookup"><span data-stu-id="3cacc-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="3cacc-181">**cArgv**</span><span class="sxs-lookup"><span data-stu-id="3cacc-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-182">Argc à extraction automatique par défaut.</span><span class="sxs-lookup"><span data-stu-id="3cacc-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-183">**pArgv**</span><span class="sxs-lookup"><span data-stu-id="3cacc-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-184">Pointeur vers un pointeur vers le argv à extraction automatique par défaut \[ \] .</span><span class="sxs-lookup"><span data-stu-id="3cacc-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-185">**fDestructive**</span><span class="sxs-lookup"><span data-stu-id="3cacc-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-186">Indicateur qui réduit l’espace disque nécessaire lorsque la propriété a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="3cacc-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3cacc-187">**iCurrentFolder**</span><span class="sxs-lookup"><span data-stu-id="3cacc-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="3cacc-188">Si **fDestructive** a la valeur **true**, extraire uniquement le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="3cacc-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3cacc-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cacc-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cacc-190">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="3cacc-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="3cacc-191">**Extraction**</span><span class="sxs-lookup"><span data-stu-id="3cacc-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
