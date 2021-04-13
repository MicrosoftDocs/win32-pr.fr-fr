---
title: DefaultAction, propriété
description: La propriété DefaultAction d’un objet décrit la méthode principale de manipulation de l’objet à partir du point de vue de l’utilisateur. La propriété DefaultAction d’un objet doit être un verbe ou une expression verbale abrégée.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309465"
---
# <a name="defaultaction-property"></a>DefaultAction, propriété

La propriété **DefaultAction** d’un objet décrit la méthode principale de manipulation de l’objet à partir du point de vue de l’utilisateur. La propriété **DefaultAction** d’un objet doit être un verbe ou une expression verbale abrégée.

La propriété **DefaultAction** est récupérée en appelant [**IAccessible :: \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Pour exécuter l’action par défaut d’un objet, les clients appellent [**IAccessible :: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

Certains objets n’ont pas d’actions par défaut, et certains objets ont une action par défaut associée à sa propriété [**value**](value-property.md) , comme dans les exemples suivants :

-   Une case à cocher activée a une action par défaut « décocher » et une valeur « activé ».
-   Une case à cocher désactivée a une action par défaut « vérifier » et une valeur « désactivée ».
-   Un bouton intitulé « Print » a une action par défaut « Press », sans valeur.
-   Un contrôle de texte statique ou un contrôle d’édition qui affiche « Printer » n’a pas d’action par défaut, mais a la valeur « Printer ».

 

 




