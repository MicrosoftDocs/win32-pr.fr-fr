---
description: Les valeurs sont utilisées par le paramètre dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319830"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="17a72-103">\_option de connexion wlx \_ \_ xxx</span><span class="sxs-lookup"><span data-stu-id="17a72-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="17a72-104">\[L' \_ \_ option de connexion wlx \_ xxx constante n’est plus disponible pour une utilisation à partir de Windows Server 2008 et Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="17a72-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="17a72-105">Les valeurs de l' **\_ option de connexion wlx \_ \_ xxx** sont utilisées par le paramètre *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="17a72-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="17a72-106">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17a72-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="17a72-107">Une fois la connexion établie, votre DLL GINA peut utiliser cette valeur pour spécifier l’option suivante.</span><span class="sxs-lookup"><span data-stu-id="17a72-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="17a72-108">Constante</span><span class="sxs-lookup"><span data-stu-id="17a72-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="17a72-109">Description</span><span class="sxs-lookup"><span data-stu-id="17a72-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="17a72-110"><dt>**\_profil d’accès d’ouverture de session wlx \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17a72-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="17a72-111">Spécifie que Winlogon ne doit pas charger de profil pour l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="17a72-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="17a72-112">Dans ce cas, soit votre DLL GINA chargera le profil, soit l’utilisateur n’a pas besoin d’un profil.</span><span class="sxs-lookup"><span data-stu-id="17a72-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="17a72-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17a72-113">Requirements</span></span>



| <span data-ttu-id="17a72-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17a72-114">Requirement</span></span> | <span data-ttu-id="17a72-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="17a72-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17a72-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a72-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17a72-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17a72-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17a72-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17a72-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17a72-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17a72-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="17a72-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="17a72-120">End of client support</span></span><br/>    | <span data-ttu-id="17a72-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="17a72-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="17a72-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="17a72-122">End of server support</span></span><br/>    | <span data-ttu-id="17a72-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17a72-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="17a72-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="17a72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a72-125"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a72-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




