---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration pour lui demander d’effectuer une initialisation globale, en particulier l’allocation de mémoire.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Message CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972050"
---
# <a name="cpl_init-message"></a><span data-ttu-id="7af58-103">Message d’initialisation de CPL \_</span><span class="sxs-lookup"><span data-stu-id="7af58-103">CPL\_INIT message</span></span>

<span data-ttu-id="7af58-104">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour lui demander d’effectuer une initialisation globale, en particulier l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="7af58-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="7af58-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7af58-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af58-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7af58-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7af58-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7af58-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7af58-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7af58-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7af58-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7af58-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af58-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7af58-110">Return value</span></span>

<span data-ttu-id="7af58-111">Si l’initialisation est réussie, la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doit retourner une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7af58-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="7af58-112">Sinon, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="7af58-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="7af58-113">Si [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retourne la valeur zéro, l’application de contrôle met fin à la communication et libère la dll contenant l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="7af58-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af58-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7af58-114">Remarks</span></span>

<span data-ttu-id="7af58-115">Comme il s’agit de la seule façon pour une application du panneau de configuration de signaler une condition d’erreur, l’application doit allouer de la mémoire en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="7af58-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="7af58-116">Ce message est envoyé immédiatement après le chargement de la DLL contenant l’application.</span><span class="sxs-lookup"><span data-stu-id="7af58-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af58-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7af58-117">Requirements</span></span>



| <span data-ttu-id="7af58-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7af58-118">Requirement</span></span> | <span data-ttu-id="7af58-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7af58-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7af58-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7af58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7af58-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7af58-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7af58-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7af58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7af58-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7af58-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7af58-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7af58-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af58-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af58-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af58-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7af58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af58-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="7af58-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
