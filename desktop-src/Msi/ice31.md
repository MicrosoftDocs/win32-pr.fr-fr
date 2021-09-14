---
description: ICE31 valide tous les styles de polices prédéfinis utilisés dans les contrôles qui affichent du texte. Il vérifie également que la propriété DefaultUIFont fait référence à un style de police valide.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021580"
---
# <a name="ice31"></a>ICE31

ICE31 valide tous les styles de polices prédéfinis utilisés dans les [contrôles](controls.md) qui affichent du texte. Il vérifie également que la propriété [**DefaultUIFont**](defaultuifont.md) fait référence à un style de police valide.

Les contrôles peuvent avoir un style de police prédéfini comme décrit dans [Ajout de contrôles et de texte](adding-controls-and-text.md). Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&*style*} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée.

ICE31 vérifie la colonne de texte pour chaque contrôle dans la [table de contrôle](control-table.md) afin de vérifier qu’il existe une entrée valide dans la [table TextStyle](textstyle-table.md).

ICE31 ignore le [contrôle ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Résultats

ICE31 publie un message d’erreur pour les styles non définis, les noms de style trop longs, une table de style de filtre (TextStyle) manquante et des balises de style sans accolade fermante.

ICE31 publie un avertissement si la balise de style n’est pas au début de la ligne, ou si un contrôle a plusieurs balises de style.

## <a name="example"></a>Exemple

ICE31 publie les erreurs suivantes pour l’exemple illustré :

-   Le contrôle DialogB. Control1 utilise le style TextStyle BadStyle non défini.
-   Le contrôle DialogB. Control2 utilise le style TextStyle BadStyle non défini.
-   L’accolade fermante du style de texte est manquante dans le contrôle DialogB. Control6.
-   Le contrôle DialogB. Control3 spécifie un style de texte qui est trop long pour être valide.

ICE31 publie l’avertissement suivant pour l’exemple illustré :

-   La balise de style texte dans DialogB. Control4 n’a aucun effet. Voulez-vous vraiment qu’elle apparaisse sous forme de texte ?

[Table de contrôle](control-table.md) (partielle)



| Boîte de dialogue  | Control  | Texte                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boîte de dialogue | Control0 | { \\ OKStyle} il s’agit du texte à afficher.                                                                                                                             |
| Boîte de dialogue | Control1 | {&OKStyle} Il s’agit du texte à afficher.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Il s’agit du texte à afficher.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle} il s’agit du texte à afficher.                                                                                                                            |
| DialogB | Control3 | {&style qui est supérieur à 72 caractères et, par conséquent, ne peut pas être un style même si vous l’avez géré pour l’obtenir dans la table TextStyle} Il s’agit du texte à afficher. |
| DialogB | Control4 | Avertissement { \\ OKStyle} il s’agit du texte à afficher.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle} {&OKStyle} il s’agit du texte à afficher.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle il s’agit du texte à afficher.                                                                                                                             |



 

[Table TextStyle](textstyle-table.md) (partielle)



| TextStyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



