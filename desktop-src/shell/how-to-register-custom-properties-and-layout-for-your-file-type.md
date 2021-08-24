---
description: Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier. Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier, procédez comme suit.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Comment inscrire des propriétés personnalisées et une disposition pour votre type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9388965a781d4104ae13de689b72208a8b69e213a758c9b34552c03bb938453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714899"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Comment inscrire des propriétés personnalisées et une disposition pour votre type de fichier

Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier.

Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Choisissez parmi les quatre modèles de disposition : alpha, bêta, gamma ou Delta.

### <a name="step-2"></a>Étape 2 :

Tenez compte des règles de mise en forme suivantes, qui s’appliquent également aux quatre modèles de disposition :

-   La propriété 1 est toujours affichée dans une plus grande taille de police. Taille de police importante généralement utilisée pour le nom de l’élément, mais peut également être utilisée pour la propriété d’ancrage ou d’autre élément.
-   La propriété 4 est destinée aux extraits des modèles de disposition alpha, bêta et gamma. Cette propriété est allouée en plus de l’espace dans ces modèles et s’affiche dans une couleur de police grise, par opposition aux autres propriétés, afin de les aider à se mettre en évidence.
-   Les mesures en pixels ci-dessous se trouvent en pixels relatifs, et la taille comprend l’icône/la miniature à gauche des propriétés et l’espace entre l’icône/la miniature et le rectangle de sélection.
-   La plupart des propriétés ont une taille d’affichage minimale. Par conséquent, ils ne s’affichent pas s’il n’y a pas suffisamment d’espace pour une taille de vue particulière. La taille minimale est généralement de 100 pixels de largeur.
-   Chaque modèle de disposition définit le nombre de lignes et le nombre de propriétés dans chaque ligne.

### <a name="step-3"></a>Étape 3 :

Choisissez les propriétés que vous souhaitez afficher dans la mise en page et la propriété que vous souhaitez afficher dans chaque emplacement. Lorsque vous choisissez la propriété à afficher à chaque position dans la disposition, tenez compte de la longueur typique de la propriété, de son importance pour l’utilisateur et de la nécessité de la supprimer lorsque la taille de la fenêtre est trop petite pour contenir toutes les propriétés.

### <a name="step-4"></a>Étape 4 :

Inscrivez un modèle de disposition et une liste de propriétés pour votre type de fichier ou type d’élément en ajoutant les clés suivantes sous la clé de Registre ProgID pour le type de fichier ou l’élément (dans cet exemple, pour le type de fichier. xyz).

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Étape 5 :

Respectez les instructions de mise en forme suivantes pour l’inscription des propriétés :

-   Chaque inscription commence par `prop:`
-   Chaque propriété requiert le nom complet de la propriété.
-   Les propriétés sont séparées par un point-virgule sans espace.
-   Les propriétés sont affichées dans l’ordre défini par le modèle de disposition sélectionné.
-   `~` indique que l’étiquette de la propriété ne doit pas être affichée.
-   `~System.LayoutPattern.PlaceHolder` doit être utilisé si vous souhaitez laisser vide une propriété qui est spécifiée dans le modèle de disposition.

L’exemple de clé de Registre suivant illustre ces instructions de mise en forme.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

Les valeurs possibles pour (ContentViewModeForBrowse) sont les suivantes : `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



