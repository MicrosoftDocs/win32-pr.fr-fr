---
title: Propriété KeyboardShortcut
description: La propriété KeyboardShortcut décrit une touche ou une combinaison de touches qui active un objet accessible spécifié.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cc82525bcfedbd370eebcfa6df078f5c98cfff7baf13d1e7e454648c054c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859969"
---
# <a name="keyboardshortcut-property"></a>Propriété KeyboardShortcut

La propriété **KeyboardShortcut** décrit une touche ou une combinaison de touches qui active un objet accessible spécifié.

La propriété **KeyboardShortcut** est récupérée en appelant [**IAccessible :: obten \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).

La chaîne Récupérée décrit une *touche de raccourci* (également appelée raccourci clavier) ou une *touche d’accès* *rapide*(également appelée « *mnémonique*»). Une touche d’accès est un caractère souligné dans le texte d’un menu, d’un élément de menu ou d’une étiquette d’un contrôle tel qu’un bouton de commande.

La chaîne Récupérée doit contenir le nom de la clé avec la ou les touches de modification. La chaîne doit être au format suivant afin que les clients puissent l’analyser facilement : \[ \[ touche de modification \] + \[ ... \] + \] nom de clé.

Voici quelques exemples : ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAJ + retour arrière ou retour arrière.

Le tableau suivant répertorie les touches de modification.



| Touche de modification | Description                        |
|--------------|------------------------------------|
| Alt          | Autre touche de modification             |
| CTRL         | Touche de modification de contrôle               |
| MAJUSCULE        | Touche de modification MAJ                 |
| GAGN          | Touche Windows                   |
| FN           | Touche de fonction sur les ordinateurs portables |



 

Ne Localisez pas les chaînes de raccourcis clavier.

## <a name="handling-objects-that-have-both-key-types"></a>Gestion des objets qui ont les deux types de clés

Si un objet a à la fois une touche de raccourci et une touche d’accès rapide, la propriété **KeyboardShortcut** retourne la clé d’accès. La touche d’accès est celle qu’un utilisateur aurait appuyé lorsque l’objet ou le parent de l’objet a le focus clavier. Par exemple, l’élément de menu **Imprimer** peut avoir à la fois une touche de raccourci (Ctrl + P) et une touche d’accès rapide (P). Si un utilisateur appuie sur CTRL + P alors que le menu est actif, rien ne se produit. Toutefois, si un utilisateur appuie sur P alors que le menu est actif, il appelle la boîte de dialogue **Imprimer** de l’application. Dans ce cas, la propriété **KeyboardShortcut** est « P » pour refléter ce que l’utilisateur doit appuyer lorsque le menu a le focus clavier.

 

 




