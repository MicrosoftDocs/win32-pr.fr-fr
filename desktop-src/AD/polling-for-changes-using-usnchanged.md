---
title: Interrogation des modifications à l’aide de USNChanged
description: Les modifications de Active Directory peuvent également être obtenues en interrogeant l’attribut uSNChanged, ce qui évite les limitations du contrôle DirSync.
ms.assetid: 83bda359-09e5-4abf-8f60-9c63bccfcdd1
ms.tgt_platform: multiple
keywords:
- Interrogation des modifications à l’aide de USNChanged AD
- USNChanged AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c665d536eb3dcb0e3265a2e3abb87808ddf630510e5d0600f6185007c72bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025527"
---
# <a name="polling-for-changes-using-usnchanged"></a>Interrogation des modifications à l’aide de USNChanged

Le contrôle DirSync est puissant et efficace, mais il présente deux limitations importantes :

-   pour les applications à privilèges élevés : pour utiliser le contrôle dirsync, une application doit s’exécuter sous un compte qui possède le privilège **SE \_ SYNC \_ AGENT \_ NAME** sur le contrôleur de domaine. Peu de comptes sont tellement privilégiés. par conséquent, une application qui utilise le contrôle DirSync ne peut pas être exécutée par des utilisateurs ordinaires.
-   Aucune étendue de sous-arborescence : le contrôle DirSync retourne toutes les modifications qui se produisent dans un contexte d’appellation. Une application qui s’intéresse uniquement aux modifications apportées à une petite sous-arborescence d’un contexte d’appellation doit parcourir de nombreuses modifications non pertinentes, ce qui est inefficace à la fois pour l’application et pour le contrôleur de domaine.

Les modifications de Active Directory peuvent également être obtenues en interrogeant l’attribut [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) , ce qui évite les limitations du contrôle DirSync. Cette alternative n’est pas mieux que le contrôle DirSync dans tous les cas, car elle implique la transmission de tous les attributs lorsqu’un attribut change et qu’elle nécessite plus de travail du développeur de l’application pour gérer correctement certains scénarios d’échec. Il s’agit actuellement de la meilleure façon d’écrire certaines applications de suivi des modifications.

Lorsqu’un contrôleur de domaine modifie un objet, il définit l’attribut [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) de cet objet sur une valeur supérieure à la valeur précédente de l’attribut **uSNChanged** pour cet objet, et supérieure à la valeur actuelle de l’attribut **uSNChanged** pour tous les autres objets détenus sur ce contrôleur de domaine. Par conséquent, une application peut trouver l’objet le plus récemment modifié sur un contrôleur de domaine en recherchant l’objet avec la plus grande valeur **uSNChanged** . Le deuxième objet récemment modifié sur un contrôleur de domaine aura la deuxième valeur **uSNChanged** la plus grande, et ainsi de suite.

L’attribut [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) n’est pas répliqué. par conséquent, la lecture de l’attribut **uSNChanged** d’un objet sur deux contrôleurs de domaine différents donne généralement des valeurs différentes.

Par exemple, l’attribut [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) peut être utilisé pour suivre les modifications apportées à une sous-arborescence S. Tout d’abord, effectuez une « synchronisation complète » de la sous-arborescence S. Supposons que la plus grande valeur **uSNChanged** pour tout objet dans s est U. interrogez régulièrement tous les objets de la sous-arborescence s dont la valeur **uSNChanged** est supérieure à u. La requête retourne tous les objets qui ont été modifiés depuis la synchronisation complète. Définissez la plus grande **uSNChanged** parmi ces objets modifiés, et vous êtes prêt à interroger à nouveau.

Les subtilités de l’implémentation d’une application de synchronisation [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) sont les suivantes :

-   Utilisez l’attribut **highestCommittedUSN** de rootDSE pour lier vos filtres [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) . Autrement dit, avant de démarrer une synchronisation complète, lisez le **highestCommittedUSN** de votre contrôleur de domaine affilié. Effectuez ensuite une requête de synchronisation complète (à l’aide des résultats paginés) pour initialiser la base de données. Une fois cette valeur effectuée, stockez la valeur **highestCommittedUSN** lue avant la requête de synchronisation complète. à utiliser comme limite inférieure de l’attribut **uSNChanged** pour la synchronisation suivante. Par la suite, pour effectuer une synchronisation incrémentielle, relisez l’attribut RootDSE **highestCommittedUSN** . Interrogez ensuite les objets pertinents à l’aide des résultats paginés, dont la valeur de **uSNChanged** est supérieure à la limite inférieure de la valeur d’attribut **uSNChanged** enregistrée à partir de la synchronisation précédente. Mettez à jour la base de données à l’aide de ces informations. Lorsque vous avez terminé, mettez à jour les limites inférieures de l’attribut **uSNChanged** à partir de la valeur **highestCommittedUSN** lue avant la requête de synchronisation incrémentielle. Stockez toujours les limites inférieures de la valeur de l’attribut **uSNChanged** dans le même stockage que l’application est en cours de synchronisation avec le contenu du contrôleur de domaine.

    À la suite de cette procédure, plutôt que d’être basée sur les valeurs [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) sur les objets récupérés, vous évitez de faire en sorte que le serveur réexamine les objets mis à jour qui sont en dehors de l’ensemble applicable à l’application.

-   Étant donné que [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) est un attribut non répliqué, l’application doit se lier au même contrôleur de domaine à chaque exécution. S’il ne peut pas effectuer de liaison à ce contrôleur de domaine, il doit attendre qu’il le fasse, ou être affilié à un nouveau contrôleur de domaine et effectuer une synchronisation complète avec ce contrôleur de domaine. Lorsque l’application est affiliée à un contrôleur de domaine, elle enregistre le nom DNS de ce contrôleur de domaine dans un stockage stable, qui est le même que celui qu’elle conserve en cohérence avec le contenu du contrôleur de domaine. Ensuite, il utilise le nom DNS stocké pour établir une liaison avec le même contrôleur de domaine pour les synchronisations suivantes.
-   L’application doit détecter si le contrôleur de domaine auquel elle est actuellement affiliée a été restauré à partir d’une sauvegarde, car cela peut entraîner une incohérence. Lorsque l’application est affiliée à un contrôleur de domaine, elle met en cache l’ID d’invocation de ce contrôleur de domaine dans un stockage stable, autrement dit, le même stockage que celui-ci est cohérent avec le contenu du contrôleur de domaine. L’ID d’invocation d’un contrôleur de domaine est un GUID stocké dans **l’attribut d’invocation de** l’objet de service du contrôleur de domaine. Pour obtenir le nom unique de l’objet de service d’un contrôleur de domaine, lisez l’attribut **dsServiceName** de l’objet rootDSE.

    Sachez que lorsque le stockage stable de l’application est restauré à partir d’une sauvegarde, il n’existe aucun problème de cohérence, car le nom du contrôleur de domaine, l’ID d’invocation et les limites inférieures de la valeur de l’attribut [**uSNChanged**](/windows/desktop/ADSchema/a-usnchanged) sont stockés avec les données synchronisées avec le contenu du contrôleur de domaine.

-   Utilisez la pagination lors de l’interrogation du serveur, à la fois des synchronisations complètes et incrémentielles, afin d’éviter la possibilité de récupérer simultanément des jeux de résultats volumineux. Pour plus d’informations, consultez [spécification d’autres options de recherche](specifying-other-search-options.md).
-   Effectuez des requêtes basées sur les index pour éviter de forcer le serveur à stocker des résultats intermédiaires importants lors de l’utilisation de résultats paginés. Pour plus d’informations, consultez [attributs indexés](indexed-attributes.md).
-   En général, n’utilisez pas le tri côté serveur des résultats de recherche, ce qui peut forcer le serveur à stocker et à trier des résultats intermédiaires volumineux. Cela s’applique à la fois aux synchronisations complètes et incrémentielles. Pour plus d’informations, consultez [spécification d’autres options de recherche](specifying-other-search-options.md).
-   Ne gérez pas les conditions parentes normalement. L’application peut reconnaître un objet avant qu’il n’ait reconnu son parent. En fonction de l’application, cela peut ne pas être un problème. L’application peut toujours lire l’état actuel du parent à partir de l’annuaire.
-   Pour gérer les objets déplacés ou supprimés, stockez l’attribut [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) de chaque objet suivi. L’attribut **objectGUID** d’un objet reste inchangé, quel que soit l’emplacement où il est déplacé dans la forêt.
-   Pour gérer les objets déplacés, effectuez des synchronisations complètes périodiques ou augmentez la portée de la recherche et filtrez les modifications non intéressantes à l’extrémité du client.
-   Pour gérer les objets supprimés, effectuez des synchronisations complètes périodiques ou effectuez une recherche distincte des objets supprimés lorsque vous effectuez une synchronisation incrémentielle. Lorsque vous interrogez des objets supprimés, récupérez l' [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) des objets supprimés pour déterminer les objets à supprimer de votre base de données. Pour plus d’informations, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).
-   Sachez que les résultats de la recherche incluent uniquement les objets et les attributs que l’appelant est autorisé à lire (en fonction des descripteurs de sécurité et des DACL sur les différents objets). Pour plus d’informations, consultez [effets de la sécurité sur les requêtes](effects-of-security-on-queries.md).

Pour plus d’informations et pour obtenir un exemple de code qui illustre les principes de base d’une application de synchronisation USNChanged, consultez l' [exemple de code permettant de récupérer des modifications à l’aide de USNChanged](example-code-to-retrieve-changes-using-usnchanged.md).

 

 