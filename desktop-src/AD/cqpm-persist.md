---
title: Message CQPM_PERSIST (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour permettre à la page de lire ou d’écrire des données de requête à partir de la mémoire persistante.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Message de CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032803"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="48cb1-104">CQPM \_ conserver le message</span><span class="sxs-lookup"><span data-stu-id="48cb1-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="48cb1-105">Le message **CQPM \_ Persist** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour permettre à la page de lire ou d’écrire des données de requête à partir de la mémoire persistante.</span><span class="sxs-lookup"><span data-stu-id="48cb1-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="48cb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48cb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48cb1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48cb1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48cb1-108">Contient une valeur différente de zéro pour lire les données de la requête ou zéro pour écrire les données de la requête.</span><span class="sxs-lookup"><span data-stu-id="48cb1-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="48cb1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48cb1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48cb1-110">Pointeur vers une interface [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) dans laquelle les données de la requête doivent être lues ou écrites.</span><span class="sxs-lookup"><span data-stu-id="48cb1-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48cb1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48cb1-111">Return value</span></span>

<span data-ttu-id="48cb1-112">Retourne **S \_ OK** en cas de réussite ou un code d’erreur **HRESULT** standard dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="48cb1-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="48cb1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48cb1-113">Requirements</span></span>



| <span data-ttu-id="48cb1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48cb1-114">Requirement</span></span> | <span data-ttu-id="48cb1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="48cb1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48cb1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48cb1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48cb1-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48cb1-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="48cb1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48cb1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48cb1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48cb1-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="48cb1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="48cb1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48cb1-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="48cb1-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48cb1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48cb1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48cb1-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="48cb1-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="48cb1-124">**IPersistQuery**</span><span class="sxs-lookup"><span data-stu-id="48cb1-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

