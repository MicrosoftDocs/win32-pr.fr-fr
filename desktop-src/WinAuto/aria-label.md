---
title: Erreur d’étiquette ARIA
description: Erreur d’étiquette ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032026"
---
# <a name="aria-label-error"></a><span data-ttu-id="1228c-104">Erreur d’étiquette ARIA</span><span class="sxs-lookup"><span data-stu-id="1228c-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="1228c-105">Texte</span><span class="sxs-lookup"><span data-stu-id="1228c-105">Text</span></span>

<span data-ttu-id="1228c-106">L’élément est de type **entrée**, **bouton**, **image-bouton** ou **repère** , mais n’a pas de nom accessible.</span><span class="sxs-lookup"><span data-stu-id="1228c-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="1228c-107">Type</span><span class="sxs-lookup"><span data-stu-id="1228c-107">Type</span></span>

<span data-ttu-id="1228c-108">Error</span><span class="sxs-lookup"><span data-stu-id="1228c-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="1228c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1228c-109">Description</span></span>

<span data-ttu-id="1228c-110">Cette erreur s’applique à :</span><span class="sxs-lookup"><span data-stu-id="1228c-110">This error applies to:</span></span>

-   <span data-ttu-id="1228c-111">Champs d’entrée de formulaire :</span><span class="sxs-lookup"><span data-stu-id="1228c-111">Form input fields:</span></span>
    -   <span data-ttu-id="1228c-112">Balises HTML **- \[ type d’entrée = "texte \| mot de passe case à cocher mot de passe de l’e-mail-couleur de l’émetteur de la \| \| \| \| \| \| \| page de la date \| DateHeure \| DateHeure- \| heure locale \| semaine \| mois nombre d’URL de recherche de \| \| plages \| \| " \]**, **Select**, **DataList** et **textarea**.</span><span class="sxs-lookup"><span data-stu-id="1228c-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="1228c-113">WAI-ARIA Roles (**case à cocher**, zone de **liste déroulante**, **zone** de liste, **radiogroupe**, **radio**, **zone de texte**, **arborescence**, **curseur** et **SpinButton**).</span><span class="sxs-lookup"><span data-stu-id="1228c-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="1228c-114">Images/boutons d’image/boutons</span><span class="sxs-lookup"><span data-stu-id="1228c-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="1228c-115">Balises HTML —**img**, **type d’entrée \[ = " \| bouton \] image"** et **bouton**.</span><span class="sxs-lookup"><span data-stu-id="1228c-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="1228c-116">WAI-ARIA Roles —**img** et **Button**.</span><span class="sxs-lookup"><span data-stu-id="1228c-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="1228c-117">Points de repère</span><span class="sxs-lookup"><span data-stu-id="1228c-117">Landmarks</span></span>
    -   <span data-ttu-id="1228c-118">WAI-ARIA Roles (**Region**, **Banner**, **complementaire**, **ContentInfo**, **Form**, **main**, **navigation** et **Search**).</span><span class="sxs-lookup"><span data-stu-id="1228c-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="1228c-119">AccChecker affiche cette erreur même pour les éléments pour lesquels le nom accessible est défini par défaut en fonction du contenu HTML interne (Voir l’élément de la **bannière** dans l’exemple ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="1228c-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="1228c-120">Dans ce cas, vous pouvez supprimer ces erreurs.</span><span class="sxs-lookup"><span data-stu-id="1228c-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="1228c-121">Tous les éléments d’interface utilisateur sémantiquement importants, tels que les champs de formulaire (par exemple, **Input**, **Select**, **textarea**), les images, les boutons et les points de repère (balises représentant des régions logiques) doivent avoir le nom accessible pour permettre aux lecteurs d’écran de les annoncer correctement.</span><span class="sxs-lookup"><span data-stu-id="1228c-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="1228c-122">Pour corriger cette erreur, définissez le nom accessible de l’une des manières suivantes (liste dans l’ordre de préférence).</span><span class="sxs-lookup"><span data-stu-id="1228c-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="1228c-123">Champs de formulaire : utilisez la balise **étiquette** et affectez à l’attribut **pour** la valeur **ID** du champ cible.</span><span class="sxs-lookup"><span data-stu-id="1228c-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="1228c-124">Bouton image/image : définissez l’attribut **ALT** .</span><span class="sxs-lookup"><span data-stu-id="1228c-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="1228c-125">Boutons : définissez le texte de la légende du bouton.</span><span class="sxs-lookup"><span data-stu-id="1228c-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="1228c-126">Pour tout élément :</span><span class="sxs-lookup"><span data-stu-id="1228c-126">For any element:</span></span>
    -   <span data-ttu-id="1228c-127">attribut [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : défini sur la valeur d' **ID** de l’élément contenant la chaîne de nom accessible.</span><span class="sxs-lookup"><span data-stu-id="1228c-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="1228c-128">[**Aria-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribut d’étiquette : défini sur la chaîne de nom accessible.</span><span class="sxs-lookup"><span data-stu-id="1228c-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="1228c-129">attribut [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : défini sur la chaîne de nom accessible (également créer une **info-bulle**).</span><span class="sxs-lookup"><span data-stu-id="1228c-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="1228c-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="1228c-130">Example</span></span>


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




