---
title: Interrogation des modifications à l’aide du contrôle DirSync
description: Le contrôle de synchronisation d’annuaires Active Directory Directory (DirSync) est une extension de serveur LDAP qui permet à une application de rechercher dans une partition d’annuaire des objets qui ont été modifiés depuis un état antérieur.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Interrogation des modifications à l’aide de l’AD du contrôle DirSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d105757d39bc25bd10df21ab68c4d1d1202be
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724469"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Interrogation des modifications à l’aide du contrôle DirSync

Le contrôle de synchronisation d’annuaires Active Directory Directory (DirSync) est une extension de serveur LDAP qui permet à une application de rechercher dans une partition d’annuaire des objets qui ont été modifiés depuis un état antérieur.

Utilisez le contrôle DirSync par le biais d’ADSI en spécifiant les préférences de recherche de **\_ \_ DirSync SEARCHPREFs ADS** lors de l’utilisation de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code utilisant les publicités \_ SEARCHPREF \_ DirSync](example-code-using-ads-searchpref-dirsync.md). Vous pouvez également effectuer une recherche DirSync à l’aide de l’API LDAP. Les éléments suivants décrivent l’implémentation d’ADSI, dont la plupart s’appliquent également à l’utilisation directe de LDAP, sauf comme indiqué à la fin de cette rubrique.

Lorsque vous effectuez une recherche DirSync, vous transmettez un élément de données spécifique au fournisseur (cookie) qui identifie l’état de l’annuaire au moment de la recherche DirSync précédente. Pour la première recherche, vous transmettez un cookie null, et la recherche retourne tous les objets qui correspondent au filtre. La recherche retourne également un cookie valide. Stockez le cookie dans le même stockage que celui que vous synchronisez avec le serveur de Active Directory. Lors des recherches suivantes, récupérez le cookie auprès du stockage et transmettez-le à la demande de recherche. Les résultats de la recherche incluent désormais uniquement les objets et les attributs qui ont été modifiés depuis l’état précédent identifié par le cookie. La recherche retourne également un nouveau cookie à stocker pour la recherche suivante.

Le tableau suivant répertorie les paramètres de recherche que la demande de recherche du client peut spécifier.



| Paramètre          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base de la recherche | La base d’une recherche DirSync doit être la racine d’une partition d’annuaire, qui peut être une partition de domaine, la partition de configuration ou la partition de schéma.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Étendue              | L’étendue d’une recherche DirSync doit être **la \_ \_ sous-arborescence étendue ADS**, c’est-à-dire la sous-arborescence entière de la partition. N’oubliez pas que pour la recherche d’une partition de domaine, la sous-arborescence comprend les têtes, mais pas le contenu, des partitions de configuration et de schéma. Pour interroger les modifications dans une plus petite étendue, utilisez la technique **USNChanged** au lieu de DirSync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtrer             | Vous pouvez spécifier n’importe quel filtre de recherche valide. Pour une recherche initiale avec un cookie null, les résultats incluent tous les objets qui correspondent au filtre. Pour les recherches suivantes avec un cookie valide, les résultats de la recherche incluent des données uniquement pour les objets qui correspondent au filtre et ont été modifiés depuis l’état indiqué par le cookie. Pour plus d’informations sur les filtres de recherche, consultez [création d’un filtre de requête](creating-a-query-filter.md).                                                                                                                                                                                                                                                                                                                |
| Attributs         | Vous pouvez spécifier une liste d’attributs à retourner lorsqu’une modification se produit. Pour chaque objet, les résultats initiaux incluent tous les attributs demandés définis sur l’objet. Les résultats de la recherche suivants incluent uniquement les attributs spécifiés qui ont été modifiés. Les attributs non modifiés ne sont pas inclus dans les résultats de la recherche. Dans l’implémentation ADSI, les résultats de la recherche incluent toujours les valeurs **objectGUID** et **instanceType** de chaque objet. En outre, la liste d’attributs spécifiée agit comme un filtre supplémentaire : les résultats de la recherche initiale incluent uniquement les objets qui ont au moins un des attributs spécifiés définis ; les recherches suivantes incluent uniquement les objets sur lesquels un ou plusieurs attributs ont changé (valeurs ajoutées ou supprimées). |



 

Sachez également que :

-   Pour les recherches incrémentielles, la meilleure pratique consiste à établir une liaison avec le même contrôleur de domaine que celui utilisé dans la recherche précédente, autrement dit, le contrôleur de domaine qui a généré le cookie. Si le même contrôleur de périphérique n’est pas disponible, patientez jusqu’à ce qu’il soit ou établissez une liaison à un nouveau contrôleur de service et effectuez une synchronisation complète. Stockez le nom DNS du contrôleur de domaine dans le stockage secondaire avec le cookie.

    Vous pouvez transmettre un cookie généré par un contrôleur de périphérique à un autre contrôleur de périphérique hébergeant un réplica de la même partition d’annuaire. Il n’y a aucun risque qu’un client ne puisse pas modifier à l’aide d’un cookie d’un contrôleur de périphérique sur un autre. Toutefois, il est possible que les résultats de la recherche du nouveau contrôleur de service puissent inclure les modifications signalées par l’ancien contrôleur de périphérique. dans certains cas, le nouveau contrôleur de périphérique peut retourner tous les objets et attributs, comme avec une synchronisation complète. Le client doit simplement rendre sa base de données cohérente avec les résultats de recherche signalés pour un appel DirSync donné, c’est-à-dire gérer tous les résultats incrémentiels comme s’il s’agissait de l’état le plus récent. Il n’est pas important de savoir si vous avez vu la modification avant ou si vous revenez à un état précédent, car les synchronisations incrémentielles répétées convergeront sur la cohérence.

-   Lorsqu’un objet est renommé ou déplacé, ses objets enfants, le cas échéant, ne sont pas inclus dans les résultats de la recherche, même si les noms uniques des objets enfants ont changé. De même, lorsqu’une entrée du contrôle d’accès héritable est modifiée dans un descripteur de sécurité d’objet, les objets enfants de l’objet ne sont pas inclus dans les résultats de la recherche, même si les descripteurs de sécurité des objets enfants ont changé.
-   Utilisez l’attribut **objectGUID** pour identifier les objets suivis. L' **objectGUID** de chaque objet reste inchangé, quel que soit l’emplacement où l’objet est déplacé dans la forêt.
-   Sachez que les résultats de la recherche d’une recherche DirSync indiquent l’état des objets sur un réplica de la partition d’annuaire au moment de la recherche. Cela signifie que les modifications apportées sur d’autres contrôleurs de l’utilisateur ne seront pas incluses si elles n’ont pas été répliquées sur le contrôleur de l’équipement cible. Cela signifie également que les attributs d’un objet peuvent avoir changé plusieurs fois depuis la recherche DirSync précédente, mais que la recherche n’affiche que l’état final, et non la séquence de modifications.
-   Dans l’implémentation ADSI, l’application doit gérer le cookie comme opaque et ne pas faire d’hypothèses concernant son organisation ou sa valeur interne.
-   N’oubliez pas que le client stocke le cookie, la longueur du cookie et le nom DNS du contrôleur de domaine dans le même stockage que celui qui contient les données de l’objet synchronisé. Cela garantit que le cookie et les autres paramètres restent synchronisés avec les données d’objet si le stockage est restauré à partir d’une sauvegarde.
-   Pour récupérer l’attribut [**parentGUID**](/windows/desktop/ADSchema/a-parentguid) , qui est construit pour le contrôle DirSync, il est également nécessaire de demander l’attribut [**Name**](/windows/desktop/ADSchema/a-name) .

Pour utiliser le contrôle DirSync, l’appelant doit disposer du droit « obtenir les modifications de l’annuaire » sur la racine de la partition surveillée. Par défaut, ce droit est attribué aux comptes administrateur et LocalSystem sur les contrôleurs de domaine. L’appelant doit également disposer du droit d’accès du contrôle étendu [**DS-Replication-obten-changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) . Pour plus d’informations sur l’implémentation d’un mécanisme de suivi des modifications pour les applications qui doivent s’exécuter sous un compte qui ne dispose pas de ce droit, consultez [interrogation des modifications à l’aide de USNChanged](polling-for-changes-using-usnchanged.md). Pour plus d’informations sur les privilèges, consultez [privilèges](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Récupération d’objets supprimés à l’aide d’une recherche DirSync

Les résultats de la recherche **\_ SEARCHPREF \_ DirSync de publicités** incluent automatiquement les objets supprimés (objets tombstone) qui correspondent au filtre de recherche spécifié. Toutefois, un filtre de recherche qui correspond à un objet lorsqu’il est en temps réel peut ne pas correspondre à l’objet après sa suppression. Cela est dû au fait que les objets tombstone ne conservent qu’un sous-ensemble des attributs présents sur l’objet d’origine. Par exemple, vous utiliseriez généralement le filtre suivant pour les objets utilisateur.


```C++
(&(objectClass=user)(objectCategory=person))
```



L’attribut **objectCategory** est supprimé lorsqu’un objet est supprimé, donc le filtre ci-dessus ne correspond à aucun objet tombstone. À l’inverse, l’attribut **objectClass** est conservé sur les objets tombstone, donc un filtre « (objectClass = user) » correspond aux objets utilisateur supprimés.

La liste d’attributs que vous spécifiez avec une recherche DirSync agit également comme un filtre. les résultats de la recherche incluent uniquement les objets sur lesquels un ou plusieurs des attributs spécifiés ont été modifiés depuis la recherche DirSync précédente. Si la liste d’attributs n’inclut aucun attribut conservé sur les objets tombstone, les résultats de la recherche n’incluent pas les objets tombstone. Pour gérer cela, demandez tous les attributs en spécifiant une liste d’attributs NULL ; ou vous pouvez demander l’attribut **IsDeleted** , avec la valeur **true** pour tous les objets tombstone. Les attributs de désactivation ont le bit 0x8 défini dans l’attribut **searchFlags** de la définition **attributeSchema** .

Pour plus d’informations, consultez [récupération des objets supprimés](retrieving-deleted-objects.md).

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implémentation LDAP du contrôle DirSync

Vous pouvez également effectuer une recherche DirSync en utilisant l’API LDAP avec le contrôle de [ \_ \_ DirSync \_ de l’OID du serveur LDAP](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) . Si vous utilisez l’API LDAP, spécifiez également [l' \_ \_ \_ \_ OID étendu du serveur LDAP](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) et le [serveur LDAP afficher les contrôles \_ \_ \_ \_ OID supprimés](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . Le \_ \_ contrôle de l’OID étendu du DN du serveur LDAP \_ \_ fait en sorte qu’une recherche LDAP retourne une forme étendue du nom unique qui comprend les attributs **objectGUID** et **objectSID** pour les objets principaux de sécurité tels que les utilisateurs, les groupes et les ordinateurs. Le \_ contrôle serveur LDAP \_ afficher les \_ \_ OID supprimés entraîne l’inclusion de données pour les objets supprimés dans les résultats de la recherche. N’oubliez pas que ces contrôles sont inclus automatiquement dans l’implémentation ADSI.

 

 