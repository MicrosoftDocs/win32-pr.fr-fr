---
title: Désactivation des classes et attributs existants
description: Les ajouts de schéma sont permanents.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671342"
---
# <a name="disabling-existing-classes-and-attributes"></a>Désactivation des classes et attributs existants

Les ajouts de schéma sont permanents. Vous ne pouvez pas supprimer les objets **attributeSchema** et **classSchema** . Dans un système distribué, il est difficile de garantir qu’il n’y a pas d’instance d’une classe ou d’un attribut donné. La suppression de la définition d’une classe ou d’un attribut endommage les instances existantes de cette classe ou de cet attribut.

Vous pouvez désactiver une classe ou un attribut existant en le marquant comme « défunt ». Cela n’affecte pas les instances existantes de la classe ou de l’attribut, ainsi marqué, mais empêche la création de nouvelles instances.

Les restrictions suivantes s’appliquent lors de la désactivation des classes de schéma et des attributs :

-   Vous ne pouvez pas désactiver une classe ou un attribut Category 1.
-   Vous ne pouvez pas désactiver un attribut qui est membre d’une classe qui n’est pas également désactivée. Cela est dû au fait qu’un attribut peut être requis pour la classe (non désactivé) et que la désactivation de l’attribut empêche la création de nouvelles instances de la classe.

Pour désactiver un attribut, affectez à l’attribut **IsDefunct** de son objet **attributeSchema** la **valeur true**. Lorsqu’un attribut est désactivé, il n’est pas possible de créer de nouvelles instances de l’attribut. Pour réactiver l’attribut, affectez la valeur **false** à l’attribut **IsDefunct** .

Pour désactiver une classe, affectez à l’attribut **IsDefunct** de son objet **classSchema** la **valeur true**. Lorsqu’une classe est désactivée, les nouvelles instances de la classe ne peuvent pas être créées. Pour réactiver la classe, affectez à l’attribut **IsDefunct** la **valeur false**.

La définition des objets de schéma comme défunts peut être utile dans les environnements de production. Lorsqu’une version de test d’une extension de schéma n’est plus nécessaire, marquez-la comme défunt. Vous pouvez la restaurer en supprimant l’attribut **IsDefunct** ou en affectant à la valeur de l’attribut la valeur **false**. Cela protège également contre la suppression involontaire d’un objet de schéma en le définissant sur défunt, car l’opération peut être facilement inversée.

N’oubliez pas que le serveur Active Directory ne nettoie pas les instances existantes d’un attribut ou d’une classe lorsque vous rendez un objet de schéma défunt. Si vous supprimez la propriété **IsDefunct** , toutes les instances deviennent valides et les objets normaux.

La liste suivante comprend d’autres conséquences du marquage d’un objet **attributeSchema** ou **classSchema** défunt :

-   L’ajout ou la modification d’une instance échoue.
-   Les codes d’erreur se comportent comme si une classe défunte n’existait jamais.
-   La recherche et la suppression se comportent comme si aucun objet de schéma n’avait été rendu obsolète.
-   Autorise uniquement la suppression de l’attribut entier de l’objet.

La liste suivante comprend des options supplémentaires dans un environnement de production pour réduire l’impact des extensions de schéma obsolètes :

-   Supprimez toutes les valeurs d’attribut **mayHave** d’une classe défunte.
-   Réduisez la taille de toutes les valeurs d’attribut **musthave** d’une classe défunte.
-   Supprimer un attribut défunt du catalogue global.
-   Supprimer un attribut défunt de n’importe quel index.

D’autres options de suppression des modifications de schéma indésirables dans un environnement de production sont destinées aux développeurs qui utilisent un contrôleur de domaine privé pour le test. Dans ce cas, vous pouvez :

-   « Réinitialisez » le serveur Active Directory en utilisant Dcpromo.exe pour rétrograder le contrôleur de périphérique. Une fois la rétrogradation terminée, utilisez Dcpromo.exe à nouveau pour réactiver le serveur sur un contrôleur de périphérique. Le développeur peut ensuite utiliser des scripts LDIF pour recharger les classes, les attributs et les instances d’objet requis.
-   Utilisez Ntbackup.exe pour effectuer une sauvegarde de l’état du système sur une partition de disque disponible. Redémarrez le mode de restauration du service d’annuaire sécurisé/sécurisé.

Pour les systèmes d’exploitation Windows Server 2003, lorsque vous définissez une classe ou un attribut sur défunt, vous pouvez réutiliser immédiatement les valeurs **ldapDisplayName**, **schemaIDGUID**, **OID** et **mapiId** de l’élément de schéma défunt lorsque vous créez une classe ou un attribut pour le remplacer. La version défunte de la classe ou de l’attribut est conservée dans le conteneur de schéma, mais elle est masquée dans le composant logiciel enfichable MMC. Pour réactiver l’ancien élément de schéma, affectez la valeur **false** à **IsDefunct** .

L’exemple de code LDIF suivant montre comment modifier l’attribut **IsDefunct** et modifier le RDN afin qu’il ne soit pas confondu avec la nouvelle classe que vous créez pour le remplacer.

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

Utilisez la commande suivante pour exécuter l’exemple de code LDIF sur une forêt pour un ordinateur s’exécutant sur des systèmes d’exploitation Windows Server 2003.

**ldifde/i/f RDN. ldf/c "DC = X" "DC = MyDomain, DC = com"**

(Où « DC = X » est une constante)

 

 




