---
title: Création d’un nouveau groupe
description: Joe worden, administrateur d’entreprise, doit créer un nouveau groupe.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941371"
---
# <a name="creating-a-new-group"></a>Création d’un nouveau groupe

Joe worden, administrateur d’entreprise, doit créer un nouveau groupe. Il souhaite sécuriser certaines ressources, telles que les objets de fichier, de Active Directory ou d’autres objets, en fonction de l’appartenance de ce groupe. L’exemple de code suivant montre comment créer un nouveau groupe.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Ce groupe, gestion, est créé dans l’unité d’organisation Sales. En premier lieu, Joe doit créer un objet ADSI pour l’unité d’organisation Sales. Ensuite, il doit définir l’attribut [**sAMAccountName**](/windows/desktop/AD/group-objects) sur cet objet, car il s’agit d’un attribut obligatoire pour la compatibilité descendante. Pour cet exemple, lorsque **sAMAccountName** est défini, les outils Windows NT 4,0 tels que le gestionnaire des utilisateurs voient l’attribut en tant que **Mgmt** et non **gestion**.

Enfin, Joe doit spécifier le type de groupe. Dans un domaine Windows 2000, il existe trois types de groupes : global, domaine local et universel. En outre, le groupe présente ses caractéristiques de sécurité. Un groupe peut être un groupe avec sécurité ou non sécurisé. Pour l’essentiel, les groupes à sécurité activée sont ceux qui peuvent se voir accorder ou refuser des droits d’accès aux ressources, à l’instar d’un utilisateur. L’octroi à un groupe d’un accès à un partage de fichiers, par exemple, implique que tous les membres du groupe peuvent accéder au partage de fichiers. Les listes de distribution ne peuvent pas être utilisées de la même façon : vous ne pouvez pas, par exemple, accorder à une liste de distribution le droit d’accéder à un partage de fichiers. Pendant la mise à niveau, les groupes Windows NT 4,0 sont migrés en tant que groupes à sécurité activée. Dans Active Directory, les groupes non sécurisés sont similaires aux listes de distribution dans Exchange. Par conséquent, la création de groupes ou de listes de distribution est une opération similaire dans Windows 2000. Dans le mode natif de Windows 2000 (le mode natif signifie que tous les contrôleurs de domaine d’un domaine sont des ordinateurs exécutant le serveur Windows 2000), les groupes peuvent être imbriqués à n’importe quel niveau.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération d’objets](enumerating-objects.md)
</dt> </dl>

 

 