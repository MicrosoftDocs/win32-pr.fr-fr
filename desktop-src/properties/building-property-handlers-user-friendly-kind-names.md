---
description: Le système de propriétés contient une propriété appelée System. Kind, qui divise les éléments en types en fonction de l’extension de nom de fichier, et quels utilisateurs finaux peuvent facilement identifier avec.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Utilisation des noms de genres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318902"
---
# <a name="using-kind-names"></a><span data-ttu-id="e7528-103">Utilisation des noms de genres</span><span class="sxs-lookup"><span data-stu-id="e7528-103">Using Kind Names</span></span>

<span data-ttu-id="e7528-104">Le système de propriétés contient une propriété appelée `System.Kind` , qui divise les éléments en types en fonction de l’extension de nom de fichier, et quels utilisateurs finaux peuvent facilement identifier avec.</span><span class="sxs-lookup"><span data-stu-id="e7528-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="e7528-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7528-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e7528-106">À propos de la propriété System. Kind</span><span class="sxs-lookup"><span data-stu-id="e7528-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="e7528-107">Hiérarchie des valeurs de type et inscription</span><span class="sxs-lookup"><span data-stu-id="e7528-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="e7528-108">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e7528-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="e7528-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7528-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="e7528-110">À propos de la propriété System. Kind</span><span class="sxs-lookup"><span data-stu-id="e7528-110">About the System.Kind Property</span></span>

<span data-ttu-id="e7528-111">Le genre a été introduit dans Windows Vista pour exprimer une notion plus conviviale de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="e7528-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="e7528-112">La `System.Kind` propriété divise les éléments en types et fournit un nom de type que les utilisateurs finaux peuvent identifier avec, tels que des documents, de la musique, des images, etc.</span><span class="sxs-lookup"><span data-stu-id="e7528-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="e7528-113">Par conséquent, les noms de types sont connus comme conviviaux.</span><span class="sxs-lookup"><span data-stu-id="e7528-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="e7528-114">Étant donné que la `System.Kind` propriété est définie sur la même valeur pour les éléments du même type de fichier, et associe les éléments qui ont des caractéristiques similaires à une propriété commune, le système et l’utilisateur peuvent agir sur le groupe dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="e7528-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="e7528-115">Par exemple, la `System.Kind` propriété peut être utilisée pour limiter une recherche aux éléments d’un type spécifique, afficher les propriétés les plus pertinentes pour un élément de l’affichage de contenu, ou regrouper des éléments similaires.</span><span class="sxs-lookup"><span data-stu-id="e7528-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="e7528-116">Comme Kind est une propriété de chaîne à valeurs multiples, vous pouvez avoir `audio;video` une `link;document` valeur de type ou.</span><span class="sxs-lookup"><span data-stu-id="e7528-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="e7528-117">Une `System.Kind` valeur est une liste triée de valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="e7528-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="e7528-118">Dans certains cas, il peut y avoir un seul élément dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="e7528-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="e7528-119">Dans d’autres cas, un élément peut appartenir à plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="e7528-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="e7528-120">Pour obtenir un exemple d’un élément appartenant à plusieurs genres, consultez l’exemple de clé de Registre dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e7528-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="e7528-121">Les valeurs de chaîne proviennent d’un ensemble prédéfini de valeurs connues.</span><span class="sxs-lookup"><span data-stu-id="e7528-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="e7528-122">Les valeurs sont comparées à l’aide de fonctions de comparaison de chaînes qui ne respectent pas la casse et qui ne respectent pas les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="e7528-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="e7528-123">Ces chaînes ne sont pas localisées.</span><span class="sxs-lookup"><span data-stu-id="e7528-123">These strings are not localized.</span></span>

<span data-ttu-id="e7528-124">Certains noms de types sont déjà associés à des propriétés et des modèles de disposition.</span><span class="sxs-lookup"><span data-stu-id="e7528-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="e7528-125">Par exemple, les éléments associés à `Kind.Picture` et les éléments associés à `Kind.Document` affichent des propriétés différentes, même lorsqu’ils sont dans la même vue, en raison des propriétés et des modèles de disposition qui sont déjà associés à ces deux noms de genres.</span><span class="sxs-lookup"><span data-stu-id="e7528-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="e7528-126">Chaque genre d’élément peut être associé à l’un des quatre modèles de disposition uniques qui définit le nombre de propriétés affichées pour chaque élément et leur disposition.</span><span class="sxs-lookup"><span data-stu-id="e7528-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="e7528-127">Pour plus d’informations, consultez [affichage du contenu basé sur l’Association type ou type de fichier](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7528-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="e7528-128">Hiérarchie des valeurs de type et inscription</span><span class="sxs-lookup"><span data-stu-id="e7528-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="e7528-129">Une `Kind` valeur doit représenter l’une des valeurs de la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="e7528-129">A `Kind` value must represent one of the values in the following list.</span></span>

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

<span data-ttu-id="e7528-130">Les gestionnaires de propriétés peuvent déclarer leur `System.Kind` propriété de manière statique par le biais du Registre, ou ils peuvent fournir la valeur dynamiquement par le biais de leur code, comme c’est le cas avec une propriété standard.</span><span class="sxs-lookup"><span data-stu-id="e7528-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="e7528-131">Pour définir la propriété de manière statique `Kind` , une entrée de valeur **reg \_ SZ** est ajoutée sous la clé de Registre **KindMap** , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e7528-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

<span data-ttu-id="e7528-132">Notez que `Kind` peut être une valeur unique ou plusieurs valeurs dans une chaîne délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e7528-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="e7528-133">Lorsque vous fournissez plusieurs valeurs, la valeur la plus spécifique `Kind` est indiquée en premier avec les éléments suivants les moins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e7528-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="e7528-134">Dans l’exemple, contact est nommé en premier, car il est hiérarchiquement plus spécifique que les communications.</span><span class="sxs-lookup"><span data-stu-id="e7528-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="e7528-135">L' **élément** de valeur est supposé et ne doit pas être explicitement fourni.</span><span class="sxs-lookup"><span data-stu-id="e7528-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7528-136">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e7528-136">Additional Resources</span></span>

-   <span data-ttu-id="e7528-137">Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](./props-system-kind.md) et [System. KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="e7528-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="e7528-138">Pour plus d’informations sur la création de nouveaux ou l’utilisation des types de fichiers existants, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e7528-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7528-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7528-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7528-140">Fonctionnement des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="e7528-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="e7528-141">Utilisation des listes de propriétés</span><span class="sxs-lookup"><span data-stu-id="e7528-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="e7528-142">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="e7528-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="e7528-143">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="e7528-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="e7528-144">Meilleures pratiques pour le gestionnaire de propriétés et FAQ</span><span class="sxs-lookup"><span data-stu-id="e7528-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
