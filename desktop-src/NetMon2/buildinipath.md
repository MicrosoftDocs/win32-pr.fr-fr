---
description: La fonction BuildINIPath retourne un chemin d’accès complet à un fichier INI qui correspond aux informations que vous entrez.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: BuildINIPath, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534605"
---
# <a name="buildinipath-function"></a><span data-ttu-id="af4df-103">BuildINIPath fonction)</span><span class="sxs-lookup"><span data-stu-id="af4df-103">BuildINIPath function</span></span>

<span data-ttu-id="af4df-104">La fonction **BuildINIPath** retourne un chemin d’accès complet à un fichier ini qui correspond aux informations que vous entrez.</span><span class="sxs-lookup"><span data-stu-id="af4df-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="af4df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af4df-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="af4df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af4df-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="af4df-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="af4df-108">Mémoire tampon qui reçoit le nom de fichier INI complet.</span><span class="sxs-lookup"><span data-stu-id="af4df-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="af4df-109">*IniFileName*</span><span class="sxs-lookup"><span data-stu-id="af4df-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="af4df-110">Nom du fichier INI (nom de fichier complet moins l’extension de nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="af4df-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af4df-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af4df-111">Return value</span></span>

<span data-ttu-id="af4df-112">Si la fonction réussit, la valeur de retour est un pointeur vers le nom de fichier INI complet.</span><span class="sxs-lookup"><span data-stu-id="af4df-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="af4df-113">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="af4df-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="af4df-114">Notes</span><span class="sxs-lookup"><span data-stu-id="af4df-114">Remarks</span></span>

<span data-ttu-id="af4df-115">Le chemin d’accès retourné par cette fonction est un chemin d’accès complet à un fichier INI qui correspond aux informations que vous entrez.</span><span class="sxs-lookup"><span data-stu-id="af4df-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="af4df-116">Par exemple, si vous entrez XNS ou TCP, la fonction génère un chemin d’accès vers Xns.ini ou Tcp.ini, respectivement.</span><span class="sxs-lookup"><span data-stu-id="af4df-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="af4df-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af4df-117">Requirements</span></span>



| <span data-ttu-id="af4df-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af4df-118">Requirement</span></span> | <span data-ttu-id="af4df-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="af4df-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af4df-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af4df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af4df-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af4df-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="af4df-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af4df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af4df-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af4df-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af4df-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="af4df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af4df-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="af4df-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="af4df-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af4df-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="af4df-127"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af4df-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="af4df-128">DLL</span><span class="sxs-lookup"><span data-stu-id="af4df-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af4df-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af4df-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




