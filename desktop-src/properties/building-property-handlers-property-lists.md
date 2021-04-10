---
description: Après avoir évalué votre stratégie de propriété, vous devez déterminer les propriétés à afficher dans l’interface utilisateur de l’Explorateur Windows, et où.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Utilisation des listes de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951610"
---
# <a name="using-property-lists"></a><span data-ttu-id="72ecb-103">Utilisation des listes de propriétés</span><span class="sxs-lookup"><span data-stu-id="72ecb-103">Using Property Lists</span></span>

<span data-ttu-id="72ecb-104">Après avoir évalué votre stratégie de propriété, vous devez déterminer les propriétés à afficher dans l’interface utilisateur de l’Explorateur Windows, et où.</span><span class="sxs-lookup"><span data-stu-id="72ecb-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="72ecb-105">Il existe différents emplacements où les propriétés sont affichées en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72ecb-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="72ecb-106">La modification de propriété, en revanche, est uniquement activée dans la boîte de dialogue **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="72ecb-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="72ecb-107">Cette boîte de dialogue peut être appelée via le lien **modifier les propriétés** dans le **volet de visualisation** ou le menu contextuel d’un élément.</span><span class="sxs-lookup"><span data-stu-id="72ecb-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="72ecb-108">Les listes de propriétés sont des chaînes délimitées par des points-virgules qui se présentent sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="72ecb-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="72ecb-109">Le seul indicateur actuellement disponible est indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="72ecb-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="72ecb-110">Indicateur</span><span class="sxs-lookup"><span data-stu-id="72ecb-110">Flag</span></span> | <span data-ttu-id="72ecb-111">Description</span><span class="sxs-lookup"><span data-stu-id="72ecb-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="72ecb-112">N’affichez pas la propriété dans le **volet de visualisation** comme indiqué dans la valeur de clé de Registre **PreviewDetails** .</span><span class="sxs-lookup"><span data-stu-id="72ecb-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="72ecb-113">Consultez l’exemple qui suit le tableau suivant si la valeur de cette propriété n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="72ecb-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="72ecb-114">Une fois que vous avez défini une liste de propriétés, vous pouvez stocker cette chaîne dans le registre par le biais du système d' [Association de fichiers Shell](../shell/fa-file-types.md) standard sous **HKEY \_ classes \_ root.**</span><span class="sxs-lookup"><span data-stu-id="72ecb-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="72ecb-115">Le tableau suivant récapitule les valeurs des listes de propriétés qui peuvent être assignées sous la clé de Registre pour une extension de nom de fichier particulière.</span><span class="sxs-lookup"><span data-stu-id="72ecb-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72ecb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ecb-116">Value</span></span></th>
<th><span data-ttu-id="72ecb-117">Description</span><span class="sxs-lookup"><span data-stu-id="72ecb-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72ecb-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="72ecb-118">FullDetails</span></span></td>
<td><span data-ttu-id="72ecb-119">Les propriétés s’affichent sous l’onglet <strong>Détails</strong> de la boîte de dialogue <strong>Propriétés</strong> .</span><span class="sxs-lookup"><span data-stu-id="72ecb-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="72ecb-120">Il s’agit de la liste complète des propriétés prises en charge par le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="72ecb-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72ecb-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="72ecb-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="72ecb-122">Les propriétés s’affichent dans le <strong>volet de visualisation</strong>.</span><span class="sxs-lookup"><span data-stu-id="72ecb-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72ecb-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="72ecb-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="72ecb-124">Les propriétés s’affichent dans la zone de titre du <strong>volet de visualisation</strong> en regard de la miniature de l’élément.</span><span class="sxs-lookup"><span data-stu-id="72ecb-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="72ecb-125">Le nombre maximal d’entrées est de 3.</span><span class="sxs-lookup"><span data-stu-id="72ecb-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="72ecb-126">Si la liste de propriétés contient plus que le nombre maximal autorisé, les autres entrées sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="72ecb-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72ecb-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="72ecb-127">TileInfo</span></span></td>
<td><span data-ttu-id="72ecb-128">Les propriétés sont affichées lorsque l’affichage de liste est en mode <strong>mosaïques</strong> .</span><span class="sxs-lookup"><span data-stu-id="72ecb-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="72ecb-129">Le nombre maximal d’entrées est de 3.</span><span class="sxs-lookup"><span data-stu-id="72ecb-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="72ecb-130">Si la liste de propriétés contient plus que le nombre maximal autorisé, les autres entrées sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="72ecb-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72ecb-131">Cette valeur était présente dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72ecb-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72ecb-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="72ecb-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="72ecb-133">Les propriétés sont affichées pour un élément lorsque l’affichage de la liste est en mode <strong>mosaïque étendue</strong> .</span><span class="sxs-lookup"><span data-stu-id="72ecb-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72ecb-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="72ecb-134">InfoTip</span></span></td>
<td><span data-ttu-id="72ecb-135">Les propriétés sont affichées dans une info-bulle quand un utilisateur pointe sur un élément.</span><span class="sxs-lookup"><span data-stu-id="72ecb-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72ecb-136">Cette valeur était présente dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72ecb-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72ecb-137">QuickTip</span><span class="sxs-lookup"><span data-stu-id="72ecb-137">QuickTip</span></span></td>
<td><span data-ttu-id="72ecb-138">Les propriétés s’affichent lorsqu’il est difficile de récupérer des propriétés directement à partir d’un élément, par exemple lorsque l’élément doit être accessible via une connexion réseau lente.</span><span class="sxs-lookup"><span data-stu-id="72ecb-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="72ecb-139">Il est recommandé que les propriétés nommées ici, telles que le type ou la taille, ne requièrent pas l’ouverture du flux de fichier pour déterminer leur valeur.</span><span class="sxs-lookup"><span data-stu-id="72ecb-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="72ecb-140">Cette valeur était présente dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72ecb-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="72ecb-141">L’exemple ci-dessous définit la valeur PreviewDetails pour un type de fichier. Recipe, à l’aide d’un ProgID de **RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="72ecb-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="72ecb-142">Comme expliqué dans la rubrique [Association de fichiers Shell](../shell/fa-file-types.md) , les associations de fichiers peuvent être décrites pour le formulaire le plus spécifique au plus général.</span><span class="sxs-lookup"><span data-stu-id="72ecb-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="72ecb-143">Le formulaire le plus spécifique est l’extension de nom de fichier unique et le formulaire le plus générique est une clé qui s’applique à tous les fichiers et dossiers de fichiers.</span><span class="sxs-lookup"><span data-stu-id="72ecb-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="72ecb-144">Entre ces deux extrêmes, vous pouvez également définir un [ProgID](../shell/fa-progids.md) qui regroupe un ensemble d’extensions de nom de fichier (par exemple, les types. jpg et. jpeg regroupés en tant que **jpegfile**).</span><span class="sxs-lookup"><span data-stu-id="72ecb-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="72ecb-145">Quand vous définissez des listes de propriétés, vous devez les définir pour les ProgID ou, dans certains cas, des extensions de nom de fichier spécifiques.</span><span class="sxs-lookup"><span data-stu-id="72ecb-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="72ecb-146">Évitez d’utiliser des entrées étendues, telles que la clé **AllFileSystemObjects** .</span><span class="sxs-lookup"><span data-stu-id="72ecb-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72ecb-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72ecb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72ecb-148">Fonctionnement des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="72ecb-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="72ecb-149">Utilisation des noms de genres</span><span class="sxs-lookup"><span data-stu-id="72ecb-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="72ecb-150">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="72ecb-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="72ecb-151">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="72ecb-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="72ecb-152">Meilleures pratiques pour le gestionnaire de propriétés et FAQ</span><span class="sxs-lookup"><span data-stu-id="72ecb-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
