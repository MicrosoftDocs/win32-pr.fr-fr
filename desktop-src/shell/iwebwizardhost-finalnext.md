---
description: Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.
title: Méthode WebWizardHost. FinalNext (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203827"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="aff9f-103">Méthode WebWizardHost. FinalNext</span><span class="sxs-lookup"><span data-stu-id="aff9f-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="aff9f-104">Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.</span><span class="sxs-lookup"><span data-stu-id="aff9f-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aff9f-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="aff9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aff9f-106">Parameters</span></span>

<span data-ttu-id="aff9f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="aff9f-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff9f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="aff9f-108">Remarks</span></span>

<span data-ttu-id="aff9f-109">Lorsque l’Assistant affiche la dernière page HTML côté serveur et que l’utilisateur clique sur le bouton **suivant** ou **Terminer** , le serveur appelle **FinalNext** dans le gestionnaire d’événements de ce bouton.</span><span class="sxs-lookup"><span data-stu-id="aff9f-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff9f-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aff9f-110">Requirements</span></span>



| <span data-ttu-id="aff9f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aff9f-111">Requirement</span></span> | <span data-ttu-id="aff9f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="aff9f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff9f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aff9f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="aff9f-114">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aff9f-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aff9f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aff9f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="aff9f-116">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aff9f-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aff9f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="aff9f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff9f-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff9f-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aff9f-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="aff9f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aff9f-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aff9f-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




