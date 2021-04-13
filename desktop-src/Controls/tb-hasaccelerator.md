---
title: Message TB_HASACCELERATOR (commctrl. h)
description: Récupère le nombre de boutons de la barre d’outils qui contiennent le caractère d’accélérateur spécifié.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465566"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="2485b-104">TO \_ HASACCELERATOR message</span><span class="sxs-lookup"><span data-stu-id="2485b-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="2485b-105">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="2485b-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="2485b-106">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2485b-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="2485b-107">Récupère le nombre de boutons de la barre d’outils qui contiennent le caractère d’accélérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2485b-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="2485b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2485b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2485b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2485b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2485b-110">**WCHAR** représentant le caractère d’accélérateur d’entrée à tester.</span><span class="sxs-lookup"><span data-stu-id="2485b-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="2485b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2485b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2485b-112">Pointeur vers un **entier** qui reçoit le nombre de boutons qui ont le caractère d’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="2485b-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2485b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2485b-113">Return value</span></span>

<span data-ttu-id="2485b-114">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2485b-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="2485b-115">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="2485b-115">Security Considerations</span></span>

<span data-ttu-id="2485b-116">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="2485b-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="2485b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2485b-117">Remarks</span></span>

<span data-ttu-id="2485b-118">Tout d’abord, le système interroge tous les boutons de barre d’outils pour faire correspondre les accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="2485b-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="2485b-119">Si aucune correspondance n’est trouvée, le système envoie la notification [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) à la fenêtre parente, en demandant l’index du bouton qui contient le caractère d’accélérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2485b-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="2485b-120">Si le parent fournit un index, le nombre est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="2485b-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2485b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2485b-121">Requirements</span></span>



| <span data-ttu-id="2485b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2485b-122">Requirement</span></span> | <span data-ttu-id="2485b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2485b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2485b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2485b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2485b-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2485b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2485b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2485b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2485b-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2485b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2485b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2485b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2485b-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2485b-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





