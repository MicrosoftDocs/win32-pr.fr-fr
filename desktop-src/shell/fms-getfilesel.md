---
description: Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).
title: Structure FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950892"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="85c7c-103">\_GETFILESEL-structure FMS</span><span class="sxs-lookup"><span data-stu-id="85c7c-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="85c7c-104">Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="85c7c-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="85c7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85c7c-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="85c7c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="85c7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="85c7c-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="85c7c-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="85c7c-108">Type : **fileTime**</span><span class="sxs-lookup"><span data-stu-id="85c7c-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="85c7c-109">Heure et date de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="85c7c-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="85c7c-110">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="85c7c-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="85c7c-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="85c7c-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="85c7c-112">Taille, en octets, du fichier.</span><span class="sxs-lookup"><span data-stu-id="85c7c-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="85c7c-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="85c7c-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="85c7c-114">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="85c7c-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="85c7c-115">Attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="85c7c-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="85c7c-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="85c7c-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="85c7c-117">Type : **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="85c7c-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="85c7c-118">Chemin d’accès complet et nom de fichier du fichier sélectionné se terminant par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="85c7c-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85c7c-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="85c7c-119">Requirements</span></span>



| <span data-ttu-id="85c7c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85c7c-120">Requirement</span></span> | <span data-ttu-id="85c7c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="85c7c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85c7c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85c7c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85c7c-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85c7c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="85c7c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85c7c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85c7c-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85c7c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85c7c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="85c7c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c7c-127"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c7c-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c7c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85c7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c7c-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="85c7c-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




