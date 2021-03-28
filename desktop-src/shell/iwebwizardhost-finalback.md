---
description: Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.
title: Méthode WebWizardHost. FinalBack (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865841"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="0eb31-103">Méthode WebWizardHost. FinalBack</span><span class="sxs-lookup"><span data-stu-id="0eb31-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="0eb31-104">Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb31-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0eb31-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="0eb31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0eb31-106">Parameters</span></span>

<span data-ttu-id="0eb31-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0eb31-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb31-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0eb31-108">Remarks</span></span>

<span data-ttu-id="0eb31-109">Lorsque l’Assistant affiche la première page côté serveur et que l’utilisateur clique sur le bouton **précédent** , le serveur appelle **FinalBack** lorsqu’il est informé de cet événement par le gestionnaire d’événements du client.</span><span class="sxs-lookup"><span data-stu-id="0eb31-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb31-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0eb31-110">Requirements</span></span>



| <span data-ttu-id="0eb31-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0eb31-111">Requirement</span></span> | <span data-ttu-id="0eb31-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eb31-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb31-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eb31-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb31-114">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0eb31-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0eb31-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eb31-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb31-116">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0eb31-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0eb31-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0eb31-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eb31-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eb31-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0eb31-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="0eb31-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0eb31-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0eb31-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




