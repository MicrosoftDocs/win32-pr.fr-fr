---
description: Structure utilisée par la fonction SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Structure PPROTECT_FILE_ENTRY (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527498"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="0bc05-103">Structure d’entrée de \_ fichier PPROTECT \_</span><span class="sxs-lookup"><span data-stu-id="0bc05-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="0bc05-104">\[Cette structure peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0bc05-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0bc05-105">La prise en charge de cette structure a été supprimée dans Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0bc05-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0bc05-106">Utilisez à la place les fonctions prises en charge listées dans [fonctions WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="0bc05-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="0bc05-107">Structure utilisée par la fonction [**SfcGetFiles**](sfcgetfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="0bc05-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc05-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bc05-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="0bc05-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0bc05-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0bc05-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="0bc05-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="0bc05-111">Pointeur vers une valeur de chaîne contenant le nom de fichier du fichier source.</span><span class="sxs-lookup"><span data-stu-id="0bc05-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="0bc05-112">La valeur est **null** si le fichier n’a pas été renommé lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="0bc05-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="0bc05-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="0bc05-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="0bc05-114">Pointeur vers la valeur de chaîne contenant le nom de fichier de destination plus le chemin d’accès complet au fichier.</span><span class="sxs-lookup"><span data-stu-id="0bc05-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="0bc05-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="0bc05-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="0bc05-116">Pointeur vers la valeur de chaîne contenant le nom du fichier INF qui fournit les informations de mise en page.</span><span class="sxs-lookup"><span data-stu-id="0bc05-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="0bc05-117">Ce paramètre peut avoir la **valeur null** lors de l’utilisation de la disposition par défaut.</span><span class="sxs-lookup"><span data-stu-id="0bc05-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bc05-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bc05-118">Requirements</span></span>



| <span data-ttu-id="0bc05-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bc05-119">Requirement</span></span> | <span data-ttu-id="0bc05-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc05-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc05-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bc05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc05-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bc05-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0bc05-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bc05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc05-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bc05-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0bc05-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0bc05-125">End of client support</span></span><br/>    | <span data-ttu-id="0bc05-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0bc05-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="0bc05-127">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0bc05-127">End of server support</span></span><br/>    | <span data-ttu-id="0bc05-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bc05-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="0bc05-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bc05-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bc05-130"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc05-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc05-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bc05-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc05-132">**SfcGetFiles**</span><span class="sxs-lookup"><span data-stu-id="0bc05-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




