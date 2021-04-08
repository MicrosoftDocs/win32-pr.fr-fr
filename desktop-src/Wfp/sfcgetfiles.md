---
description: Répertorie les fichiers protégés.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: SfcGetFiles, fonction (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865977"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="05d14-103">SfcGetFiles fonction)</span><span class="sxs-lookup"><span data-stu-id="05d14-103">SfcGetFiles function</span></span>

<span data-ttu-id="05d14-104">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="05d14-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="05d14-105">La prise en charge de cette fonction a été supprimée dans Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="05d14-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="05d14-106">Utilisez à la place les fonctions prises en charge listées dans [fonctions WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="05d14-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="05d14-107">Répertorie les fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="05d14-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d14-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05d14-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="05d14-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05d14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d14-110">*ProtFileData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05d14-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05d14-111">Pointeur vers une structure [**d' \_ \_ entrée de fichier PPROTECT**](pprotect-file-entry.md) qui contient la liste des fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="05d14-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="05d14-112">*FileCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05d14-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05d14-113">Pointeur vers un emplacement contenant une valeur ULONG qui correspond au nombre de fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="05d14-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d14-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05d14-114">Return value</span></span>

<span data-ttu-id="05d14-115">Si la fonction réussit, la valeur de retour est STATUs \_ successful.</span><span class="sxs-lookup"><span data-stu-id="05d14-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="05d14-116">Si la fonction échoue, elle retourne le code d’erreur NTSTATUS approprié.</span><span class="sxs-lookup"><span data-stu-id="05d14-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d14-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05d14-117">Requirements</span></span>



| <span data-ttu-id="05d14-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05d14-118">Requirement</span></span> | <span data-ttu-id="05d14-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="05d14-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05d14-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05d14-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05d14-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05d14-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="05d14-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05d14-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05d14-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05d14-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05d14-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="05d14-124">End of client support</span></span><br/>    | <span data-ttu-id="05d14-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="05d14-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="05d14-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="05d14-126">End of server support</span></span><br/>    | <span data-ttu-id="05d14-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05d14-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="05d14-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="05d14-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d14-129"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="05d14-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="05d14-130">DLL</span><span class="sxs-lookup"><span data-stu-id="05d14-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05d14-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05d14-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d14-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05d14-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d14-133">**\_entrée de fichier PPROTECT \_**</span><span class="sxs-lookup"><span data-stu-id="05d14-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




