---
title: Erreur d’étiquette ARIA
description: Erreur d’étiquette ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42abee9028db8c3a4070d9b60d0650187339fc4c9ec34d0b70f720c27e973897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122319"
---
# <a name="aria-label-error"></a>Erreur d’étiquette ARIA

## <a name="text"></a>Texte

L’élément est de type **entrée**, **bouton**, **image-bouton** ou **repère** , mais n’a pas de nom accessible.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique à :

-   Champs d’entrée de formulaire :
    -   Balises HTML **- \[ type d’entrée = "texte \| mot de passe case à cocher mot de passe de l’e-mail-couleur de l’émetteur de la \| \| \| \| \| \| \| page de la date \| DateHeure \| DateHeure- \| heure locale \| semaine \| mois nombre d’URL de recherche de \| \| plages \| \| " \]**, **Select**, **DataList** et **textarea**.
    -   WAI-ARIA Roles (**case à cocher**, zone de **liste déroulante**, **zone** de liste, **radiogroupe**, **radio**, **zone de texte**, **arborescence**, **curseur** et **SpinButton**).
-   Images/boutons d’image/boutons
    -   Balises HTML —**img**, **type d’entrée \[ = " \| bouton \] image"** et **bouton**.
    -   WAI-ARIA Roles —**img** et **Button**.
-   Points de repère
    -   WAI-ARIA Roles (**Region**, **Banner**, **complementaire**, **ContentInfo**, **Form**, **main**, **navigation** et **Search**).

> [!Note]  
> AccChecker affiche cette erreur même pour les éléments pour lesquels le nom accessible est défini par défaut en fonction du contenu HTML interne (Voir l’élément de la **bannière** dans l’exemple ci-dessus). Dans ce cas, vous pouvez supprimer ces erreurs.

 

Tous les éléments d’interface utilisateur sémantiquement importants, tels que les champs de formulaire (par exemple, **Input**, **Select**, **textarea**), les images, les boutons et les points de repère (balises représentant des régions logiques) doivent avoir le nom accessible pour permettre aux lecteurs d’écran de les annoncer correctement.

Pour corriger cette erreur, définissez le nom accessible de l’une des manières suivantes (liste dans l’ordre de préférence).

-   Champs de formulaire : utilisez la balise **étiquette** et affectez à l’attribut **pour** la valeur **ID** du champ cible.
-   Bouton image/image : définissez l’attribut **ALT** .
-   Boutons : définissez le texte de la légende du bouton.
-   Pour tout élément :
    -   attribut [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : défini sur la valeur d' **ID** de l’élément contenant la chaîne de nom accessible.
    -   [**Aria-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribut d’étiquette : défini sur la chaîne de nom accessible.
    -   attribut [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : défini sur la chaîne de nom accessible (également créer une **info-bulle**).

## <a name="example"></a>Exemple


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



 

 




