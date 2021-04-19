---
description: Personnaliser le comportement de Winlogon en implémentant un fournisseur d’informations d’identification.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personnalisation de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521408"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="e44f3-103">Personnalisation de Winlogon</span><span class="sxs-lookup"><span data-stu-id="e44f3-103">Customizing Winlogon</span></span>

<span data-ttu-id="e44f3-104">Personnaliser le comportement de [*Winlogon*](/windows/desktop/SecGloss/w-gly) en implémentant un fournisseur d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="e44f3-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="e44f3-105">Pour plus d’informations sur les fournisseurs d’informations d’identification, consultez [**ICredentialProvider interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span><span class="sxs-lookup"><span data-stu-id="e44f3-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="e44f3-106">**Windows Server 2003 et Windows XP :** Les fournisseurs d’informations d’identification ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e44f3-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="e44f3-107">Les sections suivantes décrivent les façons de personnaliser Winlogon dans les versions de Windows antérieures à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e44f3-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="e44f3-108">Les DLL GINA et les packages de notification Winlogon sont ignorés dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e44f3-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="e44f3-109">Packages de notification Winlogon</span><span class="sxs-lookup"><span data-stu-id="e44f3-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="e44f3-110">Stubs GINA</span><span class="sxs-lookup"><span data-stu-id="e44f3-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="e44f3-111">Hooks GINA</span><span class="sxs-lookup"><span data-stu-id="e44f3-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="e44f3-112">Packages de notification Winlogon</span><span class="sxs-lookup"><span data-stu-id="e44f3-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="e44f3-113">Un package de notification Winlogon est une DLL qui exporte les fonctions qui gèrent les événements Winlogon.</span><span class="sxs-lookup"><span data-stu-id="e44f3-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="e44f3-114">Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle chaque package de notification pour fournir des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="e44f3-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="e44f3-115">Pour plus d’informations, consultez la page [packages de notification Winlogon](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="e44f3-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="e44f3-116">Stubs GINA</span><span class="sxs-lookup"><span data-stu-id="e44f3-116">GINA Stubs</span></span>

<span data-ttu-id="e44f3-117">Un stub [*Gina*](/windows/desktop/SecGloss/g-gly) est une DLL GINA personnalisée qui utilise les implémentations de fonction d’exportation d’une DLL GINA précédemment installée (généralement MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="e44f3-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="e44f3-118">Un stub GINA obtient des pointeurs vers chaque fonction exportée par la DLL GINA précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="e44f3-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="e44f3-119">Chaque fonction stub GINA utilise ensuite le pointeur de fonction approprié pour appeler la fonction correspondante dans la DLL GINA installée précédemment.</span><span class="sxs-lookup"><span data-stu-id="e44f3-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e44f3-120">Chaque fonction stub GINA doit appeler la fonction correspondante dans le GINA précédemment installé.</span><span class="sxs-lookup"><span data-stu-id="e44f3-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="e44f3-121">Une fonction stub GINA peut implémenter des fonctionnalités supplémentaires dans une ou plusieurs de ses fonctions d’exportation.</span><span class="sxs-lookup"><span data-stu-id="e44f3-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="e44f3-122">Par exemple, la fonction [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) d’un stub Gina peut vérifier l’heure actuelle avant d’appeler la fonction **WlxLoggedOutSAS** de l' MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="e44f3-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="e44f3-123">Si l’heure actuelle se situe dans une plage spécifique, la fonction stub peut afficher un message qui indique que l’ouverture de session n’est pas autorisée pendant cette période et retourne l' **\_ action SAS wlx \_ \_ aucun** à Winlogon.</span><span class="sxs-lookup"><span data-stu-id="e44f3-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="e44f3-124">La fonction **WlxLoggedOutSAS** de l' MsGina.dll est alors appelée uniquement pendant la période autorisée.</span><span class="sxs-lookup"><span data-stu-id="e44f3-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="e44f3-125">L’application GINA stub obtient une table de dispatch pour que Winlogon prenne en charge les fonctions via le paramètre *pWinlogonFunctions* de la fonction [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) .</span><span class="sxs-lookup"><span data-stu-id="e44f3-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="e44f3-126">L’application GINA stub peut utiliser cette table de distribution pour appeler les fonctions de prise en charge de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="e44f3-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="e44f3-127">Par exemple, une application GINA stub peut appeler la fonction [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) pour déclencher un événement de [*séquence de touches de sécurité*](/windows/desktop/SecGloss/s-gly) (SAS) lorsqu’une [*carte à puce*](/windows/desktop/SecGloss/s-gly) est insérée dans un [*lecteur*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="e44f3-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="e44f3-128">Pour plus d’informations sur la création d’un stub GINA, consultez l’exemple Gina stubs dans le \\ \\ \\ répertoire Exemples de sécurité Gina \\ GinaStub d’une installation du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="e44f3-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="e44f3-129">Tous les appels entre un GINA et Winlogon doivent se trouver dans un seul thread.</span><span class="sxs-lookup"><span data-stu-id="e44f3-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="e44f3-130">Hooks GINA</span><span class="sxs-lookup"><span data-stu-id="e44f3-130">GINA Hooks</span></span>

<span data-ttu-id="e44f3-131">Un hook GINA est un stub GINA qui, dans son implémentation de la fonction [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , remplace le pointeur de la fonction de prise en charge [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) dans la table Dispatch par un pointeur vers sa propre implémentation de la fonction **WlxDialogBoxParam** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="e44f3-132">Par conséquent, chaque fois que la GINA précédemment installée (généralement MsGina.dll) appelle la fonction **WlxDialogBoxParam** , la fonction implémentée par le hook Gina est appelée.</span><span class="sxs-lookup"><span data-stu-id="e44f3-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="e44f3-133">La fonction [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implémentée par le hook Gina peut remplacer la procédure de rappel [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) qui répond à un événement de boîte de dialogue spécifique.</span><span class="sxs-lookup"><span data-stu-id="e44f3-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="e44f3-134">Cela donne au Hook GINA un contrôle total sur l’apparence et le comportement de toutes les boîtes de dialogue que MsGina.dll crée.</span><span class="sxs-lookup"><span data-stu-id="e44f3-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="e44f3-135">Pour plus d’informations sur la création d’un hook GINA, consultez l’exemple de hooks Gina dans le \\ \\ \\ répertoire Exemples de sécurité Gina \\ GinaHook d’une installation du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="e44f3-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="e44f3-136">Tous les appels entre un GINA et Winlogon doivent se trouver dans un seul thread.</span><span class="sxs-lookup"><span data-stu-id="e44f3-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
