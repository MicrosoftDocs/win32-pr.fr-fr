---
title: Accès à une autre vue de Registre
description: Par défaut, une application 32 bits s'exécutant sur WOW64 accède à la vue de Registre 32 bits et une application 64 bits accède à la vue de Registre 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- affichages du registre de la programmation Windows 64 bits
- WOW64, programmation Windows 64 bits, affichages du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "106536223"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="7b687-105">Accès à une autre vue de Registre</span><span class="sxs-lookup"><span data-stu-id="7b687-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="7b687-106">Par défaut, une application 32 bits s'exécutant sur WOW64 accède à la vue de Registre 32 bits et une application 64 bits accède à la vue de Registre 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b687-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="7b687-107">Les indicateurs suivants permettent aux applications 32 bits d’accéder aux clés redirigées dans la vue de Registre 64 bits et aux applications 64 bits d’accéder aux clés redirigées dans l’affichage du Registre 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7b687-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="7b687-108">Ces indicateurs n’ont aucun effet sur les clés de Registre partagées.</span><span class="sxs-lookup"><span data-stu-id="7b687-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="7b687-109">Pour plus d’informations, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="7b687-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="7b687-110">Nom de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="7b687-110">Flag name</span></span>         | <span data-ttu-id="7b687-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b687-111">Value</span></span>  | <span data-ttu-id="7b687-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b687-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b687-113">CLÉ \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="7b687-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="7b687-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="7b687-114">0x0100</span></span> | <span data-ttu-id="7b687-115">Accédez à une clé 64 bits à partir d’une application 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b687-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="7b687-116">CLÉ \_ WOW64 \_ 32KEY</span><span class="sxs-lookup"><span data-stu-id="7b687-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="7b687-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="7b687-117">0x0200</span></span> | <span data-ttu-id="7b687-118">Accédez à une clé 32 bits à partir d’une application 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b687-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="7b687-119">**Windows 10 sur ARM :** Cela fait référence à la vue de Registre ARM 32 bits pour les processus ARM 32 bits et à la vue de Registre x86 32 bits pour les processus ARM64 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b687-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="7b687-120">Ces indicateurs peuvent être spécifiés dans le paramètre *samDesired* des fonctions de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b687-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="7b687-121">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="7b687-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="7b687-122">**RegDeleteKeyEx**</span><span class="sxs-lookup"><span data-stu-id="7b687-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="7b687-123">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="7b687-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="7b687-124">Vous \_ pouvez spécifier la clé WOW64 \_ 32KEY ou la clé \_ WOW64 \_ 64KEY.</span><span class="sxs-lookup"><span data-stu-id="7b687-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="7b687-125">Si les deux indicateurs sont spécifiés, la fonction échoue avec un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="7b687-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="7b687-126">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Si les deux indicateurs sont spécifiés, le comportement s de la fonction n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="7b687-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="7b687-127">La fonction [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) ne peut pas être utilisée pour accéder à une autre vue de registre.</span><span class="sxs-lookup"><span data-stu-id="7b687-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="7b687-128">Voici les meilleures pratiques pour accéder au registre à partir d’une application :</span><span class="sxs-lookup"><span data-stu-id="7b687-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="7b687-129">Une fois que l’application a accédé à une autre vue du Registre à l’aide de l’un des indicateurs, toutes les opérations suivantes (créer, supprimer ou ouvrir) sur les clés de Registre enfants doivent utiliser le même indicateur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="7b687-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="7b687-130">Dans le cas contraire, il peut y avoir un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="7b687-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="7b687-131">Pour énumérer avec précision toutes les clés dans les deux vues, effectuez l’énumération en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="7b687-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="7b687-132">La première passe doit utiliser un handle ouvert avec l’un des indicateurs, et l’autre passe doit utiliser un handle ouvert avec l’autre indicateur.</span><span class="sxs-lookup"><span data-stu-id="7b687-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="7b687-133">Les clés **Wow6432Node** et **WowAA32Node** sont réservées.</span><span class="sxs-lookup"><span data-stu-id="7b687-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="7b687-134">Pour des fins de compatibilité, les applications ne doivent pas utiliser ces clés directement.</span><span class="sxs-lookup"><span data-stu-id="7b687-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="7b687-135">Pour plus d’informations sur l’accès à l’affichage de registre de remplacement par le biais de WMI, consultez [demande de données WMI sur une plateforme 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="7b687-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b687-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b687-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b687-137">Redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="7b687-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="7b687-138">Réflexion du Registre</span><span class="sxs-lookup"><span data-stu-id="7b687-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

