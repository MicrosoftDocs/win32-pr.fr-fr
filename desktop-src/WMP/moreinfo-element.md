---
title: Élément MOREINFO
description: L’élément MOREINFO spécifie une URL vers un site Web, une adresse de messagerie ou une commande de script associée à un affichage, un clip ou une bannière.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Élément MOREINFO lecteur Windows Media
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523907"
---
# <a name="moreinfo-element"></a><span data-ttu-id="418b8-104">Élément MOREINFO</span><span class="sxs-lookup"><span data-stu-id="418b8-104">MOREINFO Element</span></span>

<span data-ttu-id="418b8-105">L’élément **moreinfo** spécifie une URL vers un site Web, une adresse de messagerie ou une commande de script associée à un affichage, un clip ou une bannière.</span><span class="sxs-lookup"><span data-stu-id="418b8-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="418b8-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="418b8-106">Attributes</span></span>

<span data-ttu-id="418b8-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="418b8-107">**HREF** (required)</span></span>

<span data-ttu-id="418b8-108">URL d’un site Web, d’une adresse de messagerie ou d’une commande de script.</span><span class="sxs-lookup"><span data-stu-id="418b8-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="418b8-109">**Indicatif**</span><span class="sxs-lookup"><span data-stu-id="418b8-109">**TARGET**</span></span>

<span data-ttu-id="418b8-110">Valeur définissant le frame ou la fenêtre dans laquelle le navigateur ouvre la page définie par l’attribut **href** .</span><span class="sxs-lookup"><span data-stu-id="418b8-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="418b8-111">Il peut s’agir d’une chaîne contenant un nom de fenêtre ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="418b8-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="418b8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="418b8-112">Value</span></span>    | <span data-ttu-id="418b8-113">Description</span><span class="sxs-lookup"><span data-stu-id="418b8-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="418b8-114">\_Occult</span><span class="sxs-lookup"><span data-stu-id="418b8-114">\_blank</span></span>  | <span data-ttu-id="418b8-115">Le document se charge dans une nouvelle fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="418b8-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="418b8-116">\_self</span><span class="sxs-lookup"><span data-stu-id="418b8-116">\_self</span></span>   | <span data-ttu-id="418b8-117">Le document se charge dans le même frame que le document actif contenant le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="418b8-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="418b8-118">\_parent</span><span class="sxs-lookup"><span data-stu-id="418b8-118">\_parent</span></span> | <span data-ttu-id="418b8-119">Le document se charge dans le frame parent immédiat du frame actuel, ou le frame actuel s’il n’y a pas de frame parent.</span><span class="sxs-lookup"><span data-stu-id="418b8-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="418b8-120">\_Retour au début</span><span class="sxs-lookup"><span data-stu-id="418b8-120">\_top</span></span>    | <span data-ttu-id="418b8-121">Le document se charge dans la fenêtre de navigateur complète, en remplaçant tous les autres frames ou documents.</span><span class="sxs-lookup"><span data-stu-id="418b8-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="418b8-122">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="418b8-122">Parent/Child Elements</span></span>



| <span data-ttu-id="418b8-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="418b8-123">Hierarchy</span></span>       | <span data-ttu-id="418b8-124">Éléments</span><span class="sxs-lookup"><span data-stu-id="418b8-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="418b8-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="418b8-125">Parent elements</span></span> | <span data-ttu-id="418b8-126">**ASX**, **entrée**, **bannière**</span><span class="sxs-lookup"><span data-stu-id="418b8-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="418b8-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="418b8-127">Child elements</span></span>  | <span data-ttu-id="418b8-128">Aucune</span><span class="sxs-lookup"><span data-stu-id="418b8-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="418b8-129">Notes</span><span class="sxs-lookup"><span data-stu-id="418b8-129">Remarks</span></span>

<span data-ttu-id="418b8-130">Cet élément spécifie une URL vers un site Web, une adresse de messagerie **ou une commande de script. L’utilisateur peut accéder à la cible de l’URL en cliquant sur le graphique ou le texte associé à l’élément MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="418b8-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="418b8-131">Les détails dépendent de l’élément parent de l’élément **moreinfo** :</span><span class="sxs-lookup"><span data-stu-id="418b8-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="418b8-132">Si l’élément **moreinfo** est l’enfant d’un élément **ASX** , l’utilisateur peut accéder à l’URL en cliquant sur le titre afficher.</span><span class="sxs-lookup"><span data-stu-id="418b8-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="418b8-133">Si l’élément **moreinfo** est l’enfant d’un élément **entry** , l’utilisateur peut accéder à l’URL en cliquant sur le titre du clip.</span><span class="sxs-lookup"><span data-stu-id="418b8-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="418b8-134">Si l’élément **moreinfo** est l’enfant d’un élément **Banner** , l’utilisateur peut accéder à l’URL en cliquant sur le graphique de la bannière.</span><span class="sxs-lookup"><span data-stu-id="418b8-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="418b8-135">Si l’attribut **href** spécifie une URL vers un site Web, le navigateur s’ouvre et accède à l’URL.</span><span class="sxs-lookup"><span data-stu-id="418b8-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="418b8-136">Si l’attribut **href** spécifie une adresse e-mail, l’application de messagerie de l’utilisateur démarre.</span><span class="sxs-lookup"><span data-stu-id="418b8-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="418b8-137">Si l’attribut **href** spécifie une commande de script, la commande de script s’exécute dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="418b8-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="418b8-138">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="418b8-138">**Note**</span></span>

<span data-ttu-id="418b8-139">Si l’élément **moreinfo** apparaît dans un fichier **ASX** ou un élément d' **entrée** , lorsque le curseur de la souris est maintenu sur le titre de l’élément d’affichage (pour un élément **ASX** ) ou sur le clip (pour un élément d' **entrée** ), l’URL définie dans l’attribut **href** peut être sélectionnée et accessible par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="418b8-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="418b8-140">L’attribut **target** définit le frame ou la fenêtre dans lequel le navigateur ouvre la page définie par l’attribut **href** .</span><span class="sxs-lookup"><span data-stu-id="418b8-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="418b8-141">Les valeurs de cet attribut suivent la syntaxe et les définitions HTML standard.</span><span class="sxs-lookup"><span data-stu-id="418b8-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="418b8-142">Dans le cas d’un contrôle incorporé dans une page Web, si aucun attribut **cible** n’est défini, l’URL charge la fenêtre de navigateur actuelle et remplace la page existante, ce qui signifie que le contenu s’arrête.</span><span class="sxs-lookup"><span data-stu-id="418b8-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="418b8-143">Par conséquent, il est recommandé de toujours spécifier un attribut **cible** lorsque vous incorporez le contrôle du lecteur Windows Media dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="418b8-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="418b8-144">Si le métafichier est ouvert dans le lecteur Windows Media autonome, l’attribut **cible** est ignoré et l’URL est chargée dans une fenêtre de navigateur existante.</span><span class="sxs-lookup"><span data-stu-id="418b8-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="418b8-145">Si aucune fenêtre de navigateur n’est actuellement ouverte, l’URL est chargée dans une nouvelle fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="418b8-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="418b8-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="418b8-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="418b8-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="418b8-147">Requirements</span></span>



| <span data-ttu-id="418b8-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="418b8-148">Requirement</span></span> | <span data-ttu-id="418b8-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="418b8-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="418b8-150">Version</span><span class="sxs-lookup"><span data-stu-id="418b8-150">Version</span></span><br/> | <span data-ttu-id="418b8-151">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="418b8-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="418b8-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="418b8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418b8-153">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="418b8-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="418b8-154">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="418b8-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





