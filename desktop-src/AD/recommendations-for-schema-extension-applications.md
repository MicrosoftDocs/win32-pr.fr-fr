---
title: Recommandations pour les applications d’extension de schéma
description: Cette rubrique contient des recommandations relatives aux applications d’extension de schéma.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Recommandations pour les applications d’extension de schéma AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101429"
---
# <a name="recommendations-for-schema-extension-applications"></a>Recommandations pour les applications d’extension de schéma

Outre les conditions préalables, les meilleures pratiques suivantes sont recommandées pour les applications d’extension de schéma :

-   Recherchez le contrôleur de schéma. Établissez une liaison avec le schéma sur le contrôleur de bus qui est le contrôleur de schéma. Évitez de modifier inutilement le rôle de contrôleur de schéma entre les contrôleurs de schéma. Pour effectuer une liaison au conteneur de schéma sur le contrôleur de schéma. Pour plus d’informations, consultez [Configuration requise pour l’installation d’une extension de schéma](prerequisites-for-installing-a-schema-extension.md).
-   Avant d’effectuer une action, vérifiez la propriété **allowedChildClassesEffective** du conteneur de schéma pour vérifier que vous pouvez créer des attributs et/ou des classes. Si **attributeSchema** et **classSchema** ne sont pas des valeurs dans cette propriété, vous ne disposez pas des droits suffisants pour ajouter des attributs ou des classes au schéma. Pour plus d’informations, consultez [exemple de code pour la vérification des droits de création d’objets de schéma](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Vérifiez que la mise à jour du schéma autorisée est correctement définie dans le Registre du contrôleur de schéma. Pour créer ou définir cette valeur, restaurez son état d’origine dans le cadre de la routine de nettoyage de votre application. Pour plus d’informations sur la vérification et la définition de cette valeur, consultez [la page activation des modifications de schéma sur le contrôleur de schéma](enabling-schema-changes-at-the-schema-master.md).
-   Avant d’ajouter des attributs ou des classes, assurez-vous qu’ils n’existent pas déjà. S’ils existent, vérifiez qu’il s’agit des mêmes attributs ou classes que ceux que vous ajoutez et non d’un attribut ou d’une classe créé par une personne avec une syntaxe et des propriétés différentes qui sont incompatibles avec vos attributs ou classes.

    Pour les attributs, utilisez la requête pour **CN**, **AttributeID**, **governsID**, **lDAPDisplayName** et **schemaIDGUID** pour vous assurer qu’ils ne sont pas déjà utilisés. Si vous ajoutez un ensemble d’attributs liés (un lien suivant, un lien précédent), assurez-vous que les **LinkId** s ne sont pas déjà utilisés. Requête pour **governsID** , car l’identificateur d’objet (OID) doit être unique parmi les attributs et les classes.

    Pour les classes, interrogez **CN**, **governsID**, **AttributeID**, **lDAPDisplayName** et **schemaIDGUID** pour vous assurer qu’ils ne sont pas déjà utilisés. Requête pour **AttributeID** , car l’OID doit être unique parmi les classes et les attributs.

    Pour plus d’informations sur la vérification des collisions de noms, consultez [exemple de code pour la détection des collisions de noms de schéma](example-code-for-detecting-schema-naming-collisions.md).

    S’il existe des attributs ou des classes qui sont en conflit avec vos nouveaux attributs ou classes, votre application ne doit pas appliquer vos modifications de schéma.

-   Si une telle collision existe, votre application ne doit pas appliquer vos modifications de schéma. Il se peut que l’administrateur de schéma doive résoudre le conflit, puis exécuter à nouveau votre application. Vous pouvez également utiliser un **lDAPDisplayName** différent ; Toutefois, toutes les applications qui utilisent l’attribut ou l’objet doivent être conscientes de cette modification. Pour éviter les collisions d’OID, obtenez un OID auprès d’une autorité d’inscription de noms ISO.
-   Si votre application dépend des attributs ou des classes qu’elle a ajoutés, mettez à jour le cache de schéma avant d’ajouter les nouveaux attributs ou classes qui dépendent de ces attributs ou classes. N’oubliez pas que l’attribut opérationnel **schemaUpdateNow** est synchrone. Autrement dit, l’appel de la méthode [**IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) se bloque jusqu’à ce que le cache du schéma soit mis à jour. Lorsque l’appel est retourné, le cache de schéma a été mis à jour et les nouveaux attributs et/ou classes sont accessibles.

    Pour plus d’informations sur la mise à jour du cache de schéma, consultez [l’exemple de code pour la mise à jour du cache de schéma](example-code-for-updating-the-schema-cache.md).

 

 