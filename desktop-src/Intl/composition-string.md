---
description: La chaîne de composition est le texte actuel dans la fenêtre de composition.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Chaîne de composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cb63163ca9a8076edc4d01053e4baeffc619c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240413"
---
# <a name="composition-string"></a>Chaîne de composition

La chaîne de composition est le texte actuel dans la fenêtre de composition. Il s’agit du texte que l’IME convertit en caractères finaux. Chaque chaîne de composition se compose d’une ou plusieurs « clauses ». Une clause est la plus petite combinaison de caractères que l’IME peut convertir en caractère final. Pour récupérer et définir la chaîne de composition, l’application appelle les fonctions [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) et [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) , respectivement.

Lorsque l’utilisateur entre du texte dans la fenêtre de composition, l’IME effectue le suivi de l’état de la chaîne de composition. Cet État comprend des informations sur les attributs, les informations sur les clauses, les informations de frappe et la position du curseur. L’application peut récupérer l’état de la composition à l’aide de la fonction [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) .

Les informations d’attribut sont rendues dans un tableau de valeurs 8 bits qui spécifie l’état des caractères dans la chaîne de composition. Tous les caractères d’une clause doivent avoir le même attribut. Le tableau inclut une valeur pour chaque octet de la chaîne, y compris un octet pour le lead et le deuxième octet de tous les caractères codés sur deux octets de la chaîne. Pour chaque valeur du tableau, les bits 0 à 3 peuvent être une combinaison des valeurs suivantes.



| Valeur                      | Signification                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| \_entrée attr                | Caractère entré par l’utilisateur. L’IME n’a pas encore pu convertir ce caractère.                           |
| \_erreur d’entrée attr \_         | Caractère d’erreur que l’IME ne peut pas convertir. Par exemple, l’IME ne peut pas réunir des consonnes. |
| \_cible attr \_ convertie    | Caractère sélectionné par l’utilisateur, puis converti par l’IME.                                             |
| ATTR \_ converti            | Caractère que l’IME a déjà converti.                                                             |
| \_NOTCONVERTED cible d’attr \_ | Caractère en cours de conversion. L’utilisateur a sélectionné ce caractère, mais l’IME ne l’a pas encore converti.     |
| \_FIXEDCONVERTED attr       | Caractères que l’IME ne convertira plus.                                                           |



 

Toutes les autres valeurs sont réservées. En japonais, tout caractère non converti ayant l' \_ attribut d’entrée attr est un caractère hiragana, katakana ou alphanumérique. En coréen, cet attribut représente un caractère HANGÛL que l’IME n’a pas encore converti. Dans le chinois traditionnel et le chinois simplifié, chaque éditeur IME peut limiter son caractère dans une certaine plage.

Les informations de clause incluses dans l’état de la chaîne de composition sont un tableau de valeurs 32 bits qui spécifie les positions des clauses dans la chaîne de composition. Le tableau comprend une valeur pour chaque clause et une valeur finale qui spécifie la longueur de la chaîne complète. Chaque valeur du tableau spécifie l’offset, en octets, entre le début de la chaîne et la clause. La première valeur est toujours 0, car la première clause commence toujours au début de la chaîne. Par exemple, si une chaîne a deux clauses, les informations de la clause ont trois valeurs : la première valeur est 0, la deuxième est le décalage de la deuxième clause et la troisième valeur est la longueur de la chaîne. Pour Unicode, la position d’une clause est comptée en caractères Unicode, et la longueur d’une chaîne est la taille en caractères Unicode.

Les informations de saisie incluses dans l’état de la chaîne de composition sont une chaîne de caractères se terminant par un caractère null qui représente les caractères que l’utilisateur entre au clavier.

La position du curseur incluse dans l’état de la chaîne de composition est une valeur indiquant la position du curseur par rapport aux caractères de la chaîne de composition. La valeur est l’offset, en octets, à partir du début de la chaîne. Si cette valeur est égale à 0, le curseur est immédiatement avant le premier caractère de la chaîne. Si la valeur est égale à la longueur de la chaîne, le curseur se trouve immédiatement après le dernier caractère. Si la valeur est 1, le curseur n’est pas présent. Pour Unicode, la position et la longueur sont mesurées en caractères Unicode.

Votre application peut définir la chaîne de composition ou les éléments de l’état de la composition à l’aide de la fonction [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) . Pour vous assurer que la fenêtre de composition met à jour son apparence en fonction de ces modifications, la fonction permet à l’application d’envoyer un message de notification à la fenêtre. Les applications qui définissent une combinaison d’éléments d’état de composition désactivent généralement les notifications pour tous les appels à cette fonction, sauf le dernier, afin qu’un seul message de notification soit généré pour la fenêtre de composition.

Enfin, le contrôle d’édition prend en charge deux messages pour modifier la gestion des chaînes de composition par l’IME. Pour plus d’informations, consultez [**em \_ GETIMESTATUS**](../controls/em-getimestatus.md) et [**em \_ SETIMESTATUS**](../controls/em-setimestatus.md). Pour plus d’informations sur le contrôle d’édition, consultez [contrôle d’édition](../controls/edit-controls.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 
