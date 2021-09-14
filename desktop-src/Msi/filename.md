---
description: Le type de données filename est une chaîne de texte contenant un nom de fichier ou un dossier.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021731"
---
# <a name="filename"></a>Nom de fichier

Le type de données filename est une chaîne de texte contenant un nom de fichier ou un dossier. Par défaut, le nom de fichier est supposé utiliser la syntaxe de nom de fichier Short. c’est-à-dire, le nom de huit caractères, le point (.) et l’extension de 3 caractères. Un nom de fichier Short doit toujours être fourni, car la propriété [**SHORTFILENAMES**](shortfilenames.md) peut être définie ou le volume cible pour l’installation peut uniquement prendre en charge les noms de fichiers courts.

Pour inclure un nom de fichier long avec le nom de fichier Short, séparez-le du nom de fichier Short par une barre verticale ( \| ).

Par exemple, les deux chaînes suivantes sont valides :

-   status.txt
-   project ~1.txt\| Project Status.txt

Les noms de fichiers courts et longs ne doivent pas contenir les caractères suivants :

-   barre oblique (/) ou ( \\ )
-   point d’interrogation ( ?)
-   barre verticale ( \| )
-   Chevron droit (>)
-   Chevron gauche (<)
-   deux-points ( :)
-   astérisque ( \* )
-   guillemet (")

En outre, les noms de fichiers courts ne doivent pas contenir les caractères suivants :

-   signe plus (+)
-   virgule (,)
-   point-virgule (;)
-   signe égal (=)
-   crochet gauche ( \[ )
-   crochet droit ( \] )

Aucun espace n’est autorisé avant le séparateur de barre verticale ( \| ) pour la syntaxe de nom de fichier ou de nom de fichier long. Les noms de fichiers courts ne peuvent pas inclure d’espace, bien qu’un nom de fichier long puisse l’être. Un espace peut exister après le séparateur uniquement si le nom de fichier long du nom de fichier commence par l’espace. Aucune syntaxe de chemin d’accès complet n’est autorisée.

> [!Note]  
> Le format de la colonne de nom de fichier de la table [MsiEmbeddedUI](msiembeddedui-table.md) est semblable au type de données format FileName, sauf que le séparateur de barre verticale ( \| ) pour la syntaxe de nom de fichier ou de nom de fichier long n’est pas disponible.

 

 

 



