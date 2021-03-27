---
description: Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande annuler la suppression dans le menu fichier.
title: FM_UNDELETE_PROC pointeur de fonction (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210305"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="4a934-103">\_ \_ Pointeur de fonction proc de suppression de la suppression FM</span><span class="sxs-lookup"><span data-stu-id="4a934-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="4a934-104">Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande **annuler la suppression** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="4a934-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a934-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a934-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="4a934-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a934-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="4a934-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="4a934-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="4a934-108">Type: **HWND**</span></span>

<span data-ttu-id="4a934-109">Handle de fenêtre vers le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4a934-109">The window handle to File Manager.</span></span> <span data-ttu-id="4a934-110">Une DLL d’annulation de suppression doit utiliser ce handle pour spécifier la fenêtre propriétaire d’une boîte de dialogue ou d’une boîte de message que la DLL peut afficher.</span><span class="sxs-lookup"><span data-stu-id="4a934-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="4a934-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="4a934-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="4a934-112">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4a934-112">Type: **LPSTR**</span></span>

<span data-ttu-id="4a934-113">Adresse d’une chaîne terminée par le caractère null qui contient le nom du répertoire initial.</span><span class="sxs-lookup"><span data-stu-id="4a934-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a934-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a934-114">Return value</span></span>

<span data-ttu-id="4a934-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a934-115">Type: **DWORD**</span></span>

<span data-ttu-id="4a934-116">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4a934-116">Returns one of the following values.</span></span>



| <span data-ttu-id="4a934-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4a934-117">Return code</span></span>                                                                             | <span data-ttu-id="4a934-118">Description</span><span class="sxs-lookup"><span data-stu-id="4a934-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a934-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="4a934-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="4a934-120">Une erreur est survenue.</span><span class="sxs-lookup"><span data-stu-id="4a934-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4a934-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a934-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="4a934-122">Un fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="4a934-122">A file was undeleted.</span></span> <span data-ttu-id="4a934-123">Le gestionnaire de fichiers redessine sa fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a934-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="4a934-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="4a934-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="4a934-125">Aucun fichier n’a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="4a934-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="4a934-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a934-126">Requirements</span></span>



| <span data-ttu-id="4a934-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a934-127">Requirement</span></span> | <span data-ttu-id="4a934-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a934-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a934-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a934-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a934-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a934-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a934-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a934-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a934-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a934-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a934-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a934-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a934-134"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a934-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




