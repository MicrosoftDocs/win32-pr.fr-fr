---
description: Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant. En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.
title: Méthode WebWizardHost. SetHeaderText (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841830"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="93119-104">Méthode WebWizardHost. SetHeaderText</span><span class="sxs-lookup"><span data-stu-id="93119-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="93119-105">Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="93119-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="93119-106">En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="93119-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="93119-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93119-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="93119-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93119-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93119-109">*bstrHeaderTitle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93119-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93119-110">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="93119-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="93119-111">Chaîne contenant le titre.</span><span class="sxs-lookup"><span data-stu-id="93119-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="93119-112">*bstrHeaderSubtitle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93119-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93119-113">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="93119-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="93119-114">Chaîne contenant le sous-titre.</span><span class="sxs-lookup"><span data-stu-id="93119-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93119-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93119-115">Requirements</span></span>



| <span data-ttu-id="93119-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93119-116">Requirement</span></span> | <span data-ttu-id="93119-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="93119-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93119-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93119-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93119-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93119-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93119-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93119-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93119-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93119-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93119-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="93119-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93119-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93119-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="93119-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="93119-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93119-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93119-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
