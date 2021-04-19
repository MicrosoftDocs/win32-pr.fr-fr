---
description: Répertorie les constantes utilisées pour les API d’authentification Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes d’authentification (authentification)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538924"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="76438-103">Constantes d’authentification (authentification)</span><span class="sxs-lookup"><span data-stu-id="76438-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="76438-104">Constantes de gestion des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="76438-104">Credentials Management Constants</span></span>

<span data-ttu-id="76438-105">La gestion des informations d’identification utilise les constantes suivantes pour spécifier des tailles de chaîne maximales.</span><span class="sxs-lookup"><span data-stu-id="76438-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="76438-106">Constante</span><span class="sxs-lookup"><span data-stu-id="76438-106">Constant</span></span>                                        | <span data-ttu-id="76438-107">Description</span><span class="sxs-lookup"><span data-stu-id="76438-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76438-108">CREDUI \_ longueur maximale du \_ message \_</span><span class="sxs-lookup"><span data-stu-id="76438-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="76438-109">Nombre maximal de caractères pour le membre **pszMessageText** d’une structure [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="76438-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="76438-110">longueur de la \_ légende Max CREDUI \_ \_</span><span class="sxs-lookup"><span data-stu-id="76438-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="76438-111">Nombre maximal de caractères pour le membre **pszCaptionText** d’une structure [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="76438-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="76438-112">\_longueur maximale de la \_ \_ cible générique \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="76438-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="76438-113">Nombre maximal de caractères dans une chaîne qui spécifie un nom cible.</span><span class="sxs-lookup"><span data-stu-id="76438-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="76438-114">\_longueur maximale de la \_ cible de domaine CREDUI \_ \_</span><span class="sxs-lookup"><span data-stu-id="76438-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="76438-115">Nombre maximal de caractères dans une chaîne qui spécifie un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="76438-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="76438-116">\_longueur maximale du \_ nom d’utilisateur CREDUI \_</span><span class="sxs-lookup"><span data-stu-id="76438-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="76438-117">Nombre maximal de caractères dans une chaîne qui spécifie un nom de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76438-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="76438-118">\_longueur maximale du \_ mot de passe CREDUI \_</span><span class="sxs-lookup"><span data-stu-id="76438-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="76438-119">Nombre maximal de caractères dans une chaîne qui spécifie un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="76438-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="76438-120">Valeurs définies dans Gina</span><span class="sxs-lookup"><span data-stu-id="76438-120">Gina Defined Values</span></span>

<span data-ttu-id="76438-121">Les fonctions d’interface [*Gina*](/windows/desktop/SecGloss/g-gly) et les fonctions de prise en charge [*Winlogon*](/windows/desktop/SecGloss/w-gly) utilisent les valeurs définies suivantes.</span><span class="sxs-lookup"><span data-stu-id="76438-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="76438-122">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76438-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="76438-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="76438-123">Value</span></span>                                                              | <span data-ttu-id="76438-124">Description</span><span class="sxs-lookup"><span data-stu-id="76438-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76438-125">**\_option de connexion wlx \_ \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="76438-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="76438-126">Contient des options de connexion prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="76438-126">Contains predefined logon options.</span></span> <span data-ttu-id="76438-127">Elle est utilisée par le paramètre *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="76438-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="76438-128">**\_type wlx \_ SAS \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="76438-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="76438-129">Définit un type SAS spécifique.</span><span class="sxs-lookup"><span data-stu-id="76438-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

