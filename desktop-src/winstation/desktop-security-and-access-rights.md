---
title: Sécurité des postes de travail et droits d’accès
description: La sécurité vous permet de contrôler l’accès aux objets de bureau. Pour plus d’informations sur la sécurité, consultez Access-Control modèle.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382278"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="30cab-104">Sécurité des postes de travail et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="30cab-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="30cab-105">La sécurité vous permet de contrôler l’accès aux objets de bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="30cab-106">Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="30cab-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="30cab-107">Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un objet de bureau lorsque vous appelez la fonction [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) .</span><span class="sxs-lookup"><span data-stu-id="30cab-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="30cab-108">Si vous spécifiez NULL, le bureau obtient un descripteur de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="30cab-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="30cab-109">Les listes de contrôle d’accès dans le descripteur de sécurité par défaut d’un ordinateur de bureau proviennent de sa station de fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="30cab-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="30cab-110">Pour obtenir ou définir le descripteur de sécurité d’un objet de station Windows, appelez les fonctions [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="30cab-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="30cab-111">Lorsque vous appelez la fonction [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) ou [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30cab-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="30cab-112">Les droits d’accès valides pour les objets de bureau incluent les droits d' [accès standard](/windows/desktop/SecAuthZ/standard-access-rights) et certains droits d’accès spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="30cab-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="30cab-113">Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.</span><span class="sxs-lookup"><span data-stu-id="30cab-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="30cab-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30cab-114">Value</span></span>                       | <span data-ttu-id="30cab-115">Signification</span><span class="sxs-lookup"><span data-stu-id="30cab-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cab-116">SUPPRIMER (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="30cab-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="30cab-117">Requis pour supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="30cab-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="30cab-118">\_Contrôle de lecture (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="30cab-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="30cab-119">Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="30cab-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="30cab-120">Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la \_ sécurité du système Access \_ .</span><span class="sxs-lookup"><span data-stu-id="30cab-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="30cab-121">Pour plus d’informations, consultez [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="30cab-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="30cab-122">SYNCHRONISEr (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="30cab-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="30cab-123">Non pris en charge pour les objets de bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="30cab-124">ÉCRITURE \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="30cab-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="30cab-125">Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30cab-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="30cab-126">\_Propriétaire de l’écriture (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="30cab-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="30cab-127">Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30cab-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="30cab-128">Le tableau suivant répertorie les droits d’accès spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="30cab-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="30cab-129">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="30cab-129">Access right</span></span>                       | <span data-ttu-id="30cab-130">Description</span><span class="sxs-lookup"><span data-stu-id="30cab-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cab-131">\_CREATEMENU de bureau (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="30cab-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="30cab-132">Requis pour créer un menu sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="30cab-133">DESKTOP \_ CREATEWINDOW (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="30cab-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="30cab-134">Requis pour créer une fenêtre sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="30cab-135">\_Énumération de postes de travail (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="30cab-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="30cab-136">Requis pour que le Bureau soit énuméré.</span><span class="sxs-lookup"><span data-stu-id="30cab-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="30cab-137">\_HOOKCONTROL de bureau (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="30cab-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="30cab-138">Requis pour établir l’un des raccordements de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="30cab-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="30cab-139">\_JOURNALPLAYBACK de bureau (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="30cab-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="30cab-140">Requis pour effectuer la lecture du journal sur un ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="30cab-141">\_JOURNALRECORD de bureau (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="30cab-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="30cab-142">Requis pour effectuer l’enregistrement du journal sur un bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="30cab-143">\_READOBJECTS de bureau (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="30cab-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="30cab-144">Requis pour lire des objets sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="30cab-145">\_SWITCHDESKTOP de bureau (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="30cab-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="30cab-146">Requis pour activer le Bureau à l’aide de la fonction [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) .</span><span class="sxs-lookup"><span data-stu-id="30cab-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="30cab-147">\_WRITEOBJECTS de bureau (0x0080L)</span><span class="sxs-lookup"><span data-stu-id="30cab-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="30cab-148">Requis pour écrire des objets sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="30cab-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="30cab-149">Voici les droits d' [accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un objet de bureau contenu dans la station de fenêtre interactive de la session d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30cab-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="30cab-150">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="30cab-150">Access right</span></span></th>
<th><span data-ttu-id="30cab-151">Description</span><span class="sxs-lookup"><span data-stu-id="30cab-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30cab-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="30cab-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="30cab-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="30cab-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="30cab-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="30cab-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="30cab-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="30cab-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30cab-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="30cab-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="30cab-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="30cab-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="30cab-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="30cab-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="30cab-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="30cab-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="30cab-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="30cab-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="30cab-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="30cab-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="30cab-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="30cab-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="30cab-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="30cab-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30cab-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="30cab-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="30cab-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="30cab-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="30cab-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="30cab-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30cab-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="30cab-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="30cab-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="30cab-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="30cab-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="30cab-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="30cab-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="30cab-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="30cab-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="30cab-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="30cab-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="30cab-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="30cab-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="30cab-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="30cab-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="30cab-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="30cab-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="30cab-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="30cab-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="30cab-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="30cab-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="30cab-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="30cab-178">Vous pouvez demander le \_ \_ droit d’accès à la sécurité du système d’accès à un objet de bureau si vous souhaitez lire ou écrire la liste SACL de l’objet.</span><span class="sxs-lookup"><span data-stu-id="30cab-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="30cab-179">Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="30cab-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 