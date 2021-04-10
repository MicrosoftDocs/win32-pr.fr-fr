---
title: À propos des contrôles SysLink
description: Un contrôle SysLink est une fenêtre qui affiche le texte marqué et notifie l’application quand les utilisateurs cliquent sur ses liens hypertexte incorporés. Ce contrôle offre une alternative pratique à l’utilisation du bouton de lien de commande. Pour plus d’informations, consultez types de boutons.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031921"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="536b2-105">À propos des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="536b2-105">About SysLink Controls</span></span>

<span data-ttu-id="536b2-106">Un contrôle SysLink est une fenêtre qui affiche le texte marqué et notifie l’application quand les utilisateurs cliquent sur ses liens hypertexte incorporés.</span><span class="sxs-lookup"><span data-stu-id="536b2-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="536b2-107">Ce contrôle offre une alternative pratique à l’utilisation du [**bouton de lien de commande**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="536b2-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="536b2-108">Pour plus d’informations, consultez [types de boutons](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="536b2-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="536b2-109">Chaque contrôle SysLink peut prendre en charge plusieurs liens hypertexte et vous pouvez y accéder à l’aide d’un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="536b2-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="536b2-110">Le contrôle SysLink est défini dans la version 6 du ComCtl32.dll, et il requiert un manifeste ou une directive qui spécifie que la version 6 de la DLL doit être utilisée si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="536b2-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="536b2-111">Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="536b2-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="536b2-112">Cet article contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="536b2-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="536b2-113">Balisage SysLink</span><span class="sxs-lookup"><span data-stu-id="536b2-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="536b2-114">Attributs de lien</span><span class="sxs-lookup"><span data-stu-id="536b2-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="536b2-115">États des liens</span><span class="sxs-lookup"><span data-stu-id="536b2-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="536b2-116">Limitations relatives à l’affichage de texte bidirectionnel</span><span class="sxs-lookup"><span data-stu-id="536b2-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="536b2-117">Balisage SysLink</span><span class="sxs-lookup"><span data-stu-id="536b2-117">SysLink Markup</span></span>

<span data-ttu-id="536b2-118">Le contrôle SysLink prend en charge la balise d’ancrage ( &lt; a &gt; ), ainsi que les attributs **href** et **ID**.</span><span class="sxs-lookup"><span data-stu-id="536b2-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="536b2-119">Un **href** peut être n’importe quel protocole, tel que http, FTP et mailto.</span><span class="sxs-lookup"><span data-stu-id="536b2-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="536b2-120">Un **ID** est un nom facultatif, unique au sein d’un contrôle Syslink, et il est associé à un lien individuel.</span><span class="sxs-lookup"><span data-stu-id="536b2-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="536b2-121">Les liens reçoivent également un index de base zéro en fonction de leur position dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="536b2-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="536b2-122">Cet index est utilisé pour accéder à un lien.</span><span class="sxs-lookup"><span data-stu-id="536b2-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="536b2-123">Attributs de lien</span><span class="sxs-lookup"><span data-stu-id="536b2-123">Link Attributes</span></span>

<span data-ttu-id="536b2-124">Les attributs de chaque lien peuvent être définis dans la balise d’ancrage de chaque lien ou en envoyant le message [**LM \_ SETITEM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="536b2-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="536b2-125">La définition d’un attribut en le spécifiant dans la chaîne d’initialisation initialise simplement la valeur.</span><span class="sxs-lookup"><span data-stu-id="536b2-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="536b2-126">Vous pouvez modifier la valeur d’un attribut par le biais de l’utilisation ultérieure du message **LM \_ SETITEM** .</span><span class="sxs-lookup"><span data-stu-id="536b2-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="536b2-127">États des liens</span><span class="sxs-lookup"><span data-stu-id="536b2-127">Link States</span></span>

<span data-ttu-id="536b2-128">Les éléments de lien peuvent être dans l’un des trois États, représentés par les indicateurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="536b2-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="536b2-129">Indicateur d’État</span><span class="sxs-lookup"><span data-stu-id="536b2-129">State flag</span></span>   | <span data-ttu-id="536b2-130">Apparence et signification</span><span class="sxs-lookup"><span data-stu-id="536b2-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="536b2-131">actif \_ lis</span><span class="sxs-lookup"><span data-stu-id="536b2-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="536b2-132">Le lien a le focus clavier et appuyez sur entrée pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="536b2-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="536b2-133">LIS \_ activé</span><span class="sxs-lookup"><span data-stu-id="536b2-133">LIS\_ENABLED</span></span> | <span data-ttu-id="536b2-134">Le lien est activé.</span><span class="sxs-lookup"><span data-stu-id="536b2-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="536b2-135">LIS \_ visité</span><span class="sxs-lookup"><span data-stu-id="536b2-135">LIS\_VISITED</span></span> | <span data-ttu-id="536b2-136">L’utilisateur a déjà visité l’URL représentée par le lien.</span><span class="sxs-lookup"><span data-stu-id="536b2-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="536b2-137">Limitations relatives à l’affichage de texte bidirectionnel</span><span class="sxs-lookup"><span data-stu-id="536b2-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="536b2-138">Certains langages, tels que l’arabe ou l’hébreu, sont écrits de droite à gauche (RTL); L’anglais est écrit de gauche à droite (LTR).</span><span class="sxs-lookup"><span data-stu-id="536b2-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="536b2-139">La combinaison de RTL avec LTR est appelée texte bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="536b2-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="536b2-140">Mélanger les constructions de balisage directionnelle LTR et RTL Unicode ou HTML dans les chaînes de ressources, en tant que marqueurs de déroulement bidirectionnel pour contrôler le workflow de chaînes, peut ne pas produire le résultat attendu lors de l’utilisation d’un contrôle SysLink.</span><span class="sxs-lookup"><span data-stu-id="536b2-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="536b2-141">Par exemple, une phrase marquée LTR peut ne pas s’afficher correctement dans le contexte RTL.</span><span class="sxs-lookup"><span data-stu-id="536b2-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="536b2-142">Les contrôles SysLink ne prennent pas en charge l’affichage bidirectionnel dans tous les scénarios.</span><span class="sxs-lookup"><span data-stu-id="536b2-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="536b2-143">Utilisez un contrôle SysLink uniquement si vous savez qu’une disposition LTR ou RTL simple est appropriée.</span><span class="sxs-lookup"><span data-stu-id="536b2-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="536b2-144">Sinon, envisagez d’utiliser une technologie plus avancée telle que [mshtml](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="536b2-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 