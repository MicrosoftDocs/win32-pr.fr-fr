---
title: Gestion des erreurs dans COM (COM)
description: Gestion des erreurs dans COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923231"
---
# <a name="error-handling-in-com-com"></a>Gestion des erreurs dans COM (COM)

Presque toutes les fonctions COM et les méthodes d’interface retournent une valeur de type **HRESULT**. La valeur **HRESULT** (pour la *poignée de résultat*) est un moyen de retourner des valeurs de réussite, d’avertissement et d’erreur. Les **HRESULT** s ne sont pas des handles de tout ; Il s’agit uniquement de valeurs avec plusieurs champs encodés dans la valeur. Conformément à la spécification COM, un résultat de zéro indique Success et un résultat différent de zéro indique un échec.

Au niveau du code source, toutes les valeurs d’erreur se composent de trois parties, séparées par des traits de soulignement. La première partie est le préfixe qui identifie la fonction associée à l’erreur, la deuxième partie est E pour erreur et la troisième partie est une chaîne qui décrit la condition réelle. Par exemple, **STG \_ E \_ MEDIUMFULL** est retourné lorsqu’il n’y a pas d’espace libre sur un disque dur. Le préfixe **STG** indique la fonctionnalité de stockage, le **E** indique que le code d’état représente une erreur et **MEDIUMFULL** fournit des informations spécifiques sur l’erreur. La plupart des valeurs que vous pouvez souhaiter retourner à partir d’une méthode ou d’une fonction d’interface sont définies dans Winerror. h.

Pour plus d’informations sur la gestion des erreurs, consultez les sections suivantes :

-   [Structure des codes d’erreur COM](structure-of-com-error-codes.md)
-   [Codes dans ITF d’usine \_](codes-in-facility-itf.md)
-   [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)
-   [Gestion des erreurs COM dans Java et Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Stratégies de gestion des erreurs](error-handling-strategies.md)
-   [Gestion des erreurs inconnues](handling-unknown-errors.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes d’erreur COM](com-error-codes.md)
</dt> </dl>

 

 




