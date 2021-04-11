---
title: Modèle d’association de type de fichier et d’URI
description: Modèle d’association de type de fichier et d’URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031994"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="9ed3a-103">Modèle d’association de type de fichier et d’URI</span><span class="sxs-lookup"><span data-stu-id="9ed3a-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="9ed3a-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="9ed3a-104">Platforms</span></span>

 <span data-ttu-id="9ed3a-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="9ed3a-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="9ed3a-106">**Serveurs** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ed3a-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="9ed3a-107">Description</span><span class="sxs-lookup"><span data-stu-id="9ed3a-107">Description</span></span>

<span data-ttu-id="9ed3a-108">Le type de fichier et le modèle d’association d’URI ont été modifiés dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="9ed3a-109">Les applications ne sont plus en mesure de se définir elles-mêmes par programmation en tant que gestionnaire par défaut pour un type de fichier ou un URI.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="9ed3a-110">À la place, l’utilisateur contrôle toujours le gestionnaire par défaut pour un type de fichier ou un schéma d’URI.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9ed3a-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="9ed3a-111">Manifestation</span></span>

<span data-ttu-id="9ed3a-112">La façon dont cette modification est présentée à l’utilisateur dépend de la façon dont l’application est conçue, par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ed3a-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="9ed3a-113">De nombreuses applications vérifient s’il s’agit de la valeur par défaut chaque fois qu’elles s’exécutent et, si elles ne le sont pas, elles invitent l’utilisateur à les définir comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="9ed3a-114">Toutefois, étant donné que les applications ne peuvent pas interroger avec précision pour déterminer quelle application est le gestionnaire par défaut pour un type de fichier ou un schéma d’URI, aucune de ces opérations ne fonctionne.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="9ed3a-115">De nombreuses applications ont une boîte de dialogue ou un menu intégré ou, dans leur programme d’installation, qui spécifie les types de fichiers pour lesquels l’application doit servir de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="9ed3a-116">Toutefois, étant donné que les applications ne peuvent plus être définies par programmation comme gestionnaire par défaut pour un type de fichier ou un schéma d’URI, cela ne fonctionne plus.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="9ed3a-117">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="9ed3a-117">Mitigation</span></span>

<span data-ttu-id="9ed3a-118">Les utilisateurs peuvent effectuer plusieurs tâches pour prendre en compte les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ed3a-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="9ed3a-119">Les utilisateurs sont invités à choisir une application par défaut pour gérer les types de fichiers, les schémas d’URI ou les deux quand aucun n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="9ed3a-120">Les utilisateurs ont la possibilité de modifier leur gestionnaire par défaut après l’installation de nouvelles applications capables de gérer un type de fichier ou un schéma d’URI</span><span class="sxs-lookup"><span data-stu-id="9ed3a-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="9ed3a-121">Le panneau de configuration programmes par défaut permet aux utilisateurs de définir des valeurs par défaut pour une application, ou pour un type de fichier, un modèle d’URI, ou les deux. les applications peuvent être liées au panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="9ed3a-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="9ed3a-122">Les valeurs par défaut peuvent être modifiées à partir de l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="9ed3a-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="9ed3a-123">Solution</span><span class="sxs-lookup"><span data-stu-id="9ed3a-123">Solution</span></span>

<span data-ttu-id="9ed3a-124">Suite à ces modifications, cette recommandation d’API est fournie :</span><span class="sxs-lookup"><span data-stu-id="9ed3a-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="9ed3a-125">La fonctionnalité de certains appels de méthode au sein de l’API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) a changé et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9ed3a-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="9ed3a-126">**N'** appelez pas [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) pour déterminer si une application est la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="9ed3a-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="9ed3a-127">**N'** appelez pas [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) pour déterminer quelle application (le cas échéant) est la valeur par défaut actuelle</span><span class="sxs-lookup"><span data-stu-id="9ed3a-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="9ed3a-128">**N'** appelez pas [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) pour définir l’application par défaut</span><span class="sxs-lookup"><span data-stu-id="9ed3a-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="9ed3a-129">Les instructions à suivre sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ed3a-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="9ed3a-130">**Ne pas** interroger pour voir quelle application est le gestionnaire par défaut pour les types de fichiers ou les schémas d’URI</span><span class="sxs-lookup"><span data-stu-id="9ed3a-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="9ed3a-131">**N’essayez pas** de surveiller les modifications dans le gestionnaire par défaut pour les types de fichiers ou les schémas d’URI</span><span class="sxs-lookup"><span data-stu-id="9ed3a-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="9ed3a-132">**N’essayez pas** de définir une application en tant que gestionnaire par défaut pour les types de fichiers ou les schémas d’URI</span><span class="sxs-lookup"><span data-stu-id="9ed3a-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="9ed3a-133">**N’essayez pas** de gérer les valeurs par défaut pour les types de fichiers ou les schémas d’URI à partir d’une application</span><span class="sxs-lookup"><span data-stu-id="9ed3a-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="9ed3a-134">**S’intègrent** au panneau de [configuration définir les programmes par défaut](../shell/default-programs.md) si vous souhaitez autoriser les utilisateurs de votre application à accéder à l’interface utilisateur de gestion par défaut (l’interface utilisateur de gestion dans l’application n’est plus prise en charge)</span><span class="sxs-lookup"><span data-stu-id="9ed3a-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="9ed3a-135">L’appel de [IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permet à l’utilisateur d’accéder à la page «[définir les programmes par défaut](../shell/default-programs.md)» du panneau de configuration pour l’application spécifiée</span><span class="sxs-lookup"><span data-stu-id="9ed3a-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="9ed3a-136">Tests</span><span class="sxs-lookup"><span data-stu-id="9ed3a-136">Tests</span></span>

-   <span data-ttu-id="9ed3a-137">Test pour vérifier que les applications s’inscrivent correctement dans le panneau de configuration des programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="9ed3a-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="9ed3a-138">Testez pour vérifier que les applications s’inscrivent correctement dans la liste OpenWith pour les types de fichiers, les schémas d’URI, ou les deux, qu’ils inscrivent pour gérer</span><span class="sxs-lookup"><span data-stu-id="9ed3a-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="9ed3a-139">Test pour vérifier que les nouvelles notifications de l’application s’affichent après l’installation de votre application et que l’utilisateur appelle un type de fichier, un modèle d’URI, ou les deux, que votre application s’est inscrite pour gérer</span><span class="sxs-lookup"><span data-stu-id="9ed3a-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="9ed3a-140">Ressources</span><span class="sxs-lookup"><span data-stu-id="9ed3a-140">Resources</span></span>

-   <span data-ttu-id="9ed3a-141">[Meilleures pratiques pour les associations de type de fichier et d’URI dans les applications de bureau Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ed3a-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="9ed3a-142">Associations de types de fichier et présentation de la Conférence génération d’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="9ed3a-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 