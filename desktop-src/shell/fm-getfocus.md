---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.
title: Message FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973239"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="f8aeb-103">\_Message FM getFocus</span><span class="sxs-lookup"><span data-stu-id="f8aeb-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="f8aeb-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8aeb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8aeb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8aeb-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8aeb-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8aeb-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8aeb-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8aeb-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8aeb-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8aeb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8aeb-110">Return value</span></span>

<span data-ttu-id="f8aeb-111">Retourne le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="f8aeb-112">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-112">It can be one of the following values.</span></span>



| <span data-ttu-id="f8aeb-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f8aeb-113">Return code</span></span>                                                                                    | <span data-ttu-id="f8aeb-114">Description</span><span class="sxs-lookup"><span data-stu-id="f8aeb-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f8aeb-115"><dt>**FMFOCUS \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="f8aeb-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="f8aeb-116">Partie répertoire d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="f8aeb-117"><dt>**\_arbre FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="f8aeb-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="f8aeb-118">Partie de l’arborescence d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="f8aeb-119"><dt>**\_lecteurs FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="f8aeb-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="f8aeb-120">Barre de lecteur d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="f8aeb-121"><dt>**\_recherche FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="f8aeb-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="f8aeb-122">Fenêtre des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="f8aeb-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="f8aeb-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8aeb-123">Requirements</span></span>



| <span data-ttu-id="f8aeb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8aeb-124">Requirement</span></span> | <span data-ttu-id="f8aeb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8aeb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8aeb-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8aeb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f8aeb-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8aeb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f8aeb-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8aeb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f8aeb-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8aeb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8aeb-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8aeb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8aeb-131"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8aeb-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




