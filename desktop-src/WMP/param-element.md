---
title: PARAM, élément (kit de développement logiciel (SDK) WMP)
description: L’élément PARAM définit un paramètre personnalisé associé à une sélection ou à un élément d’une sélection.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Élément PARAM Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525629"
---
# <a name="param-element"></a><span data-ttu-id="ebf13-104">Élément PARAM</span><span class="sxs-lookup"><span data-stu-id="ebf13-104">PARAM Element</span></span>

<span data-ttu-id="ebf13-105">L’élément **param** définit un paramètre personnalisé associé à une sélection ou à un élément d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="ebf13-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="ebf13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf13-106">Parameters</span></span>

<span data-ttu-id="ebf13-107">Un paramètre peut également être associé à l’affichage plutôt qu’à un élément individuel, en plaçant cet élément directement après la balise **ASX** .</span><span class="sxs-lookup"><span data-stu-id="ebf13-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="ebf13-108">Ces éléments sont référencés par leurs noms et une valeur d’index commençant par zéro.</span><span class="sxs-lookup"><span data-stu-id="ebf13-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="ebf13-109">Cet élément **ASX** est disponible uniquement pour le lecteur Windows media version 6,01 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ebf13-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="ebf13-110">L’installation standard de Microsoft Internet Explorer 5 comprend une version compatible du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ebf13-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="ebf13-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ebf13-111">Attributes</span></span>

<span data-ttu-id="ebf13-112">**NAME**</span><span class="sxs-lookup"><span data-stu-id="ebf13-112">**NAME**</span></span>

<span data-ttu-id="ebf13-113">Nom utilisé pour accéder à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf13-113">Name used to access the parameter value.</span></span> <span data-ttu-id="ebf13-114">Le nom peut être n’importe quelle chaîne valide.</span><span class="sxs-lookup"><span data-stu-id="ebf13-114">The name can be any valid string.</span></span> <span data-ttu-id="ebf13-115">Les chaînes suivantes ont déjà été définies.</span><span class="sxs-lookup"><span data-stu-id="ebf13-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="ebf13-116">String</span><span class="sxs-lookup"><span data-stu-id="ebf13-116">String</span></span>                          | <span data-ttu-id="ebf13-117">Description</span><span class="sxs-lookup"><span data-stu-id="ebf13-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf13-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="ebf13-118">AllowShuffle</span></span>                    | <span data-ttu-id="ebf13-119">L’attribut **value** spécifie si la sélection de métafichier permet à la fonctionnalité de lecture aléatoire du lecteur Windows Media de lire les entrées dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ebf13-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="ebf13-120">L’attribut value peut avoir la **valeur** « Yes » ou « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="ebf13-121">La valeur par défaut est « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ebf13-122">CanPause</span><span class="sxs-lookup"><span data-stu-id="ebf13-122">CanPause</span></span>                        | <span data-ttu-id="ebf13-123">L’attribut **value** spécifie si l’utilisateur peut suspendre la lecture.</span><span class="sxs-lookup"><span data-stu-id="ebf13-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="ebf13-124">L’attribut value peut avoir la **valeur** « Yes » ou « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="ebf13-125">La valeur par défaut est « Yes ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ebf13-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="ebf13-126">CanSeek</span></span>                         | <span data-ttu-id="ebf13-127">L’attribut **value** spécifie si l’utilisateur peut modifier la position de lecture actuelle à l’aide de la barre de recherche, de l’avance rapide ou de l’inverse rapide.</span><span class="sxs-lookup"><span data-stu-id="ebf13-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="ebf13-128">L’attribut value peut avoir la **valeur** « Yes » ou « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="ebf13-129">La valeur par défaut est « Yes ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ebf13-130">CanSkipBack</span><span class="sxs-lookup"><span data-stu-id="ebf13-130">CanSkipBack</span></span>                     | <span data-ttu-id="ebf13-131">L’attribut **value** spécifie si l’utilisateur peut revenir à l’élément de sélection précédent en cliquant sur **précédent**.</span><span class="sxs-lookup"><span data-stu-id="ebf13-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="ebf13-132">L’attribut value peut avoir la **valeur** « Yes » ou « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="ebf13-133">La valeur par défaut est « Yes ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ebf13-134">CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="ebf13-134">CanSkipForward</span></span>                  | <span data-ttu-id="ebf13-135">L’attribut **value** spécifie si l’utilisateur peut avancer jusqu’à l’élément de sélection suivant en cliquant sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ebf13-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="ebf13-136">L’attribut value peut avoir la **valeur** « Yes » ou « no ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="ebf13-137">La valeur par défaut est « Yes ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ebf13-138">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="ebf13-138">CPRadioID</span></span>                       | <span data-ttu-id="ebf13-139">L’attribut **value** spécifie l’ID d’un flux radio fourni par un magasin en ligne de type 1.</span><span class="sxs-lookup"><span data-stu-id="ebf13-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="ebf13-140">Autrement dit, l’attribut **value** doit être égal au champ RadioID de l’un des flux radio dans le catalogue du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ebf13-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="ebf13-141">L’élément parent est l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="ebf13-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ebf13-142">Encodage</span><span class="sxs-lookup"><span data-stu-id="ebf13-142">Encoding</span></span>                        | <span data-ttu-id="ebf13-143">L’attribut **value** est défini sur « UTF-8 » pour indiquer que le métafichier est un fichier encodé en Unicode (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="ebf13-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ebf13-144">HtmlFlink</span><span class="sxs-lookup"><span data-stu-id="ebf13-144">HtmlFlink</span></span>                       | <span data-ttu-id="ebf13-145">L’attribut **value** est une chaîne fournie par un magasin de type 1 en ligne.</span><span class="sxs-lookup"><span data-stu-id="ebf13-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="ebf13-146">Le lecteur Windows Media transmet la chaîne à la méthode [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , qui est implémentée par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ebf13-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="ebf13-147">La méthode **GetItemInfo** retourne l’URL de la page Web à afficher dans le volet de **lecture à présent** du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ebf13-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="ebf13-148">La page Web a accès à toutes les méthodes que l’objet **externe** expose aux magasins de type 1.</span><span class="sxs-lookup"><span data-stu-id="ebf13-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="ebf13-149">Pour obtenir la liste de ces méthodes, consultez [objet externe pour les magasins de type 1 en ligne](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="ebf13-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="ebf13-150">HTMLView</span><span class="sxs-lookup"><span data-stu-id="ebf13-150">HTMLView</span></span>                        | <span data-ttu-id="ebf13-151">L’attribut **value** spécifie une URL qui s’affiche dans le volet de **lecture à présent** du lecteur en mode complet pendant la durée de la sélection ou l’entrée actuelle selon que l’élément parent est l’élément **ASX** ou un élément d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="ebf13-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="ebf13-152">HTMLView n’est pas pris en charge pour le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ebf13-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ebf13-153">JRN :*fieldName* \[ :*espace de noms*\]</span><span class="sxs-lookup"><span data-stu-id="ebf13-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="ebf13-154">L’attribut **value** spécifie la valeur dans laquelle le champ de journal indiqué sera défini.</span><span class="sxs-lookup"><span data-stu-id="ebf13-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="ebf13-155">La partie :*namespace* de l’attribut **Name** est facultative.</span><span class="sxs-lookup"><span data-stu-id="ebf13-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ebf13-156">Prémémoire tampon</span><span class="sxs-lookup"><span data-stu-id="ebf13-156">Prebuffer</span></span>                       | <span data-ttu-id="ebf13-157">L’attribut **value** spécifie si l’entrée de playlist suivante commence la mise en mémoire tampon avant la fin de l’entrée actuelle, ce qui permet une transition transparente.</span><span class="sxs-lookup"><span data-stu-id="ebf13-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="ebf13-158">L’attribut value peut avoir la **valeur** « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ebf13-159">ShowWhileBuffering</span><span class="sxs-lookup"><span data-stu-id="ebf13-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="ebf13-160">L’attribut **value** spécifie si un fichier image référencé par l’élément d' **entrée** actuel continue à s’afficher au-delà de la durée spécifiée pendant la mise en mémoire tampon de l’entrée de playlist suivante.</span><span class="sxs-lookup"><span data-stu-id="ebf13-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="ebf13-161">L’attribut value peut avoir la **valeur** « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="ebf13-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="ebf13-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="ebf13-162">**VALUE**</span></span>

<span data-ttu-id="ebf13-163">Valeur associée à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf13-163">Value associated with this parameter.</span></span> <span data-ttu-id="ebf13-164">Il peut s’agir d’une valeur numérique ou de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ebf13-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ebf13-165">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="ebf13-165">Parent/Child Elements</span></span>



| <span data-ttu-id="ebf13-166">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ebf13-166">Hierarchy</span></span>       | <span data-ttu-id="ebf13-167">Éléments</span><span class="sxs-lookup"><span data-stu-id="ebf13-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="ebf13-168">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ebf13-168">Parent elements</span></span> | <span data-ttu-id="ebf13-169">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="ebf13-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="ebf13-170">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ebf13-170">Child elements</span></span>  | <span data-ttu-id="ebf13-171">Aucune</span><span class="sxs-lookup"><span data-stu-id="ebf13-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="ebf13-172">Notes</span><span class="sxs-lookup"><span data-stu-id="ebf13-172">Remarks</span></span>

<span data-ttu-id="ebf13-173">Cet élément permet aux utilisateurs de placer des informations supplémentaires sur chaque clip à l’intérieur de l’élément d' **entrée** qui le contient.</span><span class="sxs-lookup"><span data-stu-id="ebf13-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="ebf13-174">Pour récupérer les informations de métadonnées spécifiées dans l' **entrée** de la playlist, utilisez le *support*. méthode **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="ebf13-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="ebf13-175">*Média*. la méthode **getItemInfo** récupère la valeur de l’attribut **value** , en fonction du nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ebf13-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="ebf13-176">Les versions précédentes du lecteur Windows Media récupèrent les informations de métadonnées spécifiées dans l' **entrée** de playlist, à l’aide de la méthode **GetMediaParameter** en fonction du nom du paramètre et d’un numéro d’index pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="ebf13-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="ebf13-177">Un paramètre peut également être associé à l’affichage plutôt qu’à un élément individuel, en plaçant cet élément directement après la balise **ASX** .</span><span class="sxs-lookup"><span data-stu-id="ebf13-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="ebf13-178">Ces éléments sont référencés par leurs noms et une valeur d’index commençant par zéro.</span><span class="sxs-lookup"><span data-stu-id="ebf13-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="ebf13-179">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="ebf13-179">**Note**</span></span>

<span data-ttu-id="ebf13-180">Cet élément **ASX** est disponible uniquement pour le lecteur Windows media version 6,01 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ebf13-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="ebf13-181">L’installation standard de Microsoft Internet Explorer 5 comprend une version compatible du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ebf13-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="ebf13-182">Exemples</span><span class="sxs-lookup"><span data-stu-id="ebf13-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="ebf13-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf13-183">Requirements</span></span>



| <span data-ttu-id="ebf13-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf13-184">Requirement</span></span> | <span data-ttu-id="ebf13-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf13-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf13-186">Version</span><span class="sxs-lookup"><span data-stu-id="ebf13-186">Version</span></span><br/> | <span data-ttu-id="ebf13-187">Le lecteur Windows Media version 7,0 ou ultérieure, le lecteur Windows Media série 9 ou une version ultérieure est requis pour les attributs de nom prédéfinis, le lecteur Windows Media 10 ou version ultérieure est requis pour les noms prédéfinis CanPause, CanSeek, CanSkipBack et CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="ebf13-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf13-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf13-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf13-189">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ebf13-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="ebf13-190">**Journalisation des données de flux**</span><span class="sxs-lookup"><span data-stu-id="ebf13-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="ebf13-191">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ebf13-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ebf13-192">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ebf13-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





