---
title: Sécurité de station Windows et droits d’accès
description: La sécurité vous permet de contrôler l’accès aux objets de station Windows. Pour plus d’informations sur la sécurité, consultez Access-Control modèle.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511079"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="4e31b-104">Sécurité de station Windows et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="4e31b-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="4e31b-105">La sécurité vous permet de contrôler l’accès aux objets de station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="4e31b-106">Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="4e31b-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="4e31b-107">Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un objet de station Windows lorsque vous appelez la fonction [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="4e31b-108">Si vous spécifiez la valeur NULL, la station Windows obtient un descripteur de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e31b-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="4e31b-109">Les listes de contrôle d’accès dans le descripteur de sécurité par défaut d’une station Windows proviennent du jeton principal ou d’emprunt d’identité du créateur.</span><span class="sxs-lookup"><span data-stu-id="4e31b-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="4e31b-110">Pour obtenir ou définir le descripteur de sécurité d’un objet de station Windows, appelez les fonctions [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="4e31b-111">Lorsque vous appelez la fonction [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e31b-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="4e31b-112">Les droits d’accès valides pour les objets de station Windows incluent les [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) et certains droits d’accès spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="4e31b-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="4e31b-113">Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.</span><span class="sxs-lookup"><span data-stu-id="4e31b-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="4e31b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e31b-114">Value</span></span>                       | <span data-ttu-id="4e31b-115">Signification</span><span class="sxs-lookup"><span data-stu-id="4e31b-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e31b-116">SUPPRIMER (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="4e31b-117">Requis pour supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e31b-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4e31b-118">\_Contrôle de lecture (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="4e31b-119">Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="4e31b-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="4e31b-120">Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la \_ sécurité du système Access \_ .</span><span class="sxs-lookup"><span data-stu-id="4e31b-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="4e31b-121">Pour plus d’informations, consultez [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="4e31b-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="4e31b-122">SYNCHRONISEr (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="4e31b-123">Non pris en charge pour les objets de station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="4e31b-124">ÉCRITURE \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="4e31b-125">Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e31b-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="4e31b-126">\_Propriétaire de l’écriture (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="4e31b-127">Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e31b-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="4e31b-128">Le tableau suivant répertorie les droits d’accès spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="4e31b-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="4e31b-129">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="4e31b-129">Access right</span></span>                        | <span data-ttu-id="4e31b-130">Description</span><span class="sxs-lookup"><span data-stu-id="4e31b-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e31b-131">WINSTA \_ tous les \_ accès (0x37F)</span><span class="sxs-lookup"><span data-stu-id="4e31b-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="4e31b-132">Tous les droits d’accès possibles pour la station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="4e31b-133">WINSTA \_ ACCESSCLIPBOARD (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="4e31b-134">Requis pour utiliser le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4e31b-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="4e31b-135">WINSTA \_ ACCESSGLOBALATOMS (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="4e31b-136">Requis pour manipuler les atomes globaux.</span><span class="sxs-lookup"><span data-stu-id="4e31b-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4e31b-137">WINSTA \_ CREATEDESKTOP (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="4e31b-138">Requis pour créer de nouveaux objets de bureau sur la station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="4e31b-139">WINSTA \_ ENUMDESKTOPS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="4e31b-140">Requis pour énumérer les objets de bureau existants.</span><span class="sxs-lookup"><span data-stu-id="4e31b-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="4e31b-141">\_Énumération WINSTA (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="4e31b-142">Requis pour que la station de fenêtre soit énumérée.</span><span class="sxs-lookup"><span data-stu-id="4e31b-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="4e31b-143">WINSTA \_ EXITWINDOWS (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="4e31b-144">Requis pour appeler correctement la fonction [**exitwindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="4e31b-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="4e31b-145">Les stations de Windows peuvent être partagées par les utilisateurs et ce type d’accès peut empêcher les autres utilisateurs d’une station Windows de se déconnecter du propriétaire de la station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="4e31b-146">WINSTA \_ READATTRIBUTES (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="4e31b-147">Requis pour lire les attributs d’un objet de station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="4e31b-148">Cet attribut comprend des paramètres de couleur et d’autres propriétés de station de fenêtre globale.</span><span class="sxs-lookup"><span data-stu-id="4e31b-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="4e31b-149">WINSTA \_ READSCREEN (0x0200L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="4e31b-150">Requis pour accéder au contenu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="4e31b-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="4e31b-151">WINSTA \_ WRITEATTRIBUTES (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="4e31b-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="4e31b-152">Requis pour modifier les attributs d’un objet de station Windows.</span><span class="sxs-lookup"><span data-stu-id="4e31b-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="4e31b-153">Les attributs incluent les paramètres de couleur et d’autres propriétés de la station de fenêtre globale.</span><span class="sxs-lookup"><span data-stu-id="4e31b-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="4e31b-154">Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour l’objet de station Windows Interactive, qui est la station Windows affectée à la session d’ouverture de session de l’utilisateur interactif.</span><span class="sxs-lookup"><span data-stu-id="4e31b-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4e31b-155">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="4e31b-155">Access right</span></span></th>
<th><span data-ttu-id="4e31b-156">Description</span><span class="sxs-lookup"><span data-stu-id="4e31b-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e31b-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="4e31b-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="4e31b-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="4e31b-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="4e31b-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4e31b-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4e31b-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4e31b-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4e31b-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="4e31b-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="4e31b-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e31b-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="4e31b-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="4e31b-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="4e31b-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="4e31b-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4e31b-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4e31b-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4e31b-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4e31b-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e31b-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4e31b-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="4e31b-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4e31b-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="4e31b-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4e31b-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4e31b-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4e31b-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e31b-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="4e31b-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="4e31b-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="4e31b-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="4e31b-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4e31b-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4e31b-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4e31b-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4e31b-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4e31b-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4e31b-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4e31b-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4e31b-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4e31b-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4e31b-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4e31b-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="4e31b-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="4e31b-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="4e31b-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="4e31b-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4e31b-183">Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un objet de station Windows non interactive.</span><span class="sxs-lookup"><span data-stu-id="4e31b-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="4e31b-184">Le système affecte les stations Windows non interactives à toutes les sessions d’ouverture de session autres que celles de l’utilisateur interactif.</span><span class="sxs-lookup"><span data-stu-id="4e31b-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4e31b-185">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="4e31b-185">Access right</span></span></th>
<th><span data-ttu-id="4e31b-186">Description</span><span class="sxs-lookup"><span data-stu-id="4e31b-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e31b-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="4e31b-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="4e31b-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="4e31b-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="4e31b-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4e31b-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4e31b-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4e31b-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4e31b-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e31b-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="4e31b-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="4e31b-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="4e31b-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="4e31b-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4e31b-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4e31b-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4e31b-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e31b-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4e31b-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="4e31b-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4e31b-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="4e31b-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4e31b-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4e31b-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4e31b-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e31b-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="4e31b-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="4e31b-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="4e31b-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="4e31b-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4e31b-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4e31b-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4e31b-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4e31b-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4e31b-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4e31b-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4e31b-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4e31b-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4e31b-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4e31b-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4e31b-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="4e31b-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4e31b-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4e31b-209">Vous pouvez demander le \_ droit accès à la sécurité du système d’accès \_ à un objet de station Windows si vous souhaitez lire ou écrire la liste SACL de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e31b-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="4e31b-210">Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="4e31b-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 