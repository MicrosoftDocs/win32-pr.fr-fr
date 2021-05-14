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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841410"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="974e2-103">\_Message FM getFocus</span><span class="sxs-lookup"><span data-stu-id="974e2-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="974e2-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="974e2-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="974e2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="974e2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974e2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="974e2-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="974e2-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="974e2-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="974e2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="974e2-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="974e2-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="974e2-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974e2-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="974e2-110">Return value</span></span>

<span data-ttu-id="974e2-111">Retourne le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="974e2-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="974e2-112">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="974e2-112">It can be one of the following values.</span></span>



| <span data-ttu-id="974e2-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="974e2-113">Return code</span></span>                                                                                    | <span data-ttu-id="974e2-114">Description</span><span class="sxs-lookup"><span data-stu-id="974e2-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="974e2-115"><dt>**FMFOCUS \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="974e2-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="974e2-116">Partie répertoire d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="974e2-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="974e2-117"><dt>**\_arbre FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="974e2-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="974e2-118">Partie de l’arborescence d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="974e2-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="974e2-119"><dt>**\_lecteurs FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="974e2-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="974e2-120">Barre de lecteur d’une fenêtre de répertoire.</span><span class="sxs-lookup"><span data-stu-id="974e2-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="974e2-121"><dt>**\_recherche FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="974e2-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="974e2-122">Fenêtre des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="974e2-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="974e2-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="974e2-123">Requirements</span></span>



| <span data-ttu-id="974e2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="974e2-124">Requirement</span></span> | <span data-ttu-id="974e2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="974e2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="974e2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="974e2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="974e2-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="974e2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="974e2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="974e2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="974e2-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="974e2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="974e2-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="974e2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="974e2-131"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="974e2-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




