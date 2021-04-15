---
title: Vue d’ensemble du didacticiel ADSI avec Visual Basic
description: Active Directory est une base de données à usage spécial \ 8212 ; il ne s’agit pas d’un remplacement du Registre.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104570596"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Vue d’ensemble du didacticiel : ADSI avec Visual Basic

> [!Note]  
> La documentation suivante fait partie d’une description de scénario étendue pour les développeurs Visual Basic. Si vous recherchez une vue d’ensemble générale de Active Directory, consultez les [documents professionnels de l’informatique sur TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Pour une analyse plus approfondie du côté développement de Active Directory, consultez [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Pour plus d’informations sur les interfaces de service Active Directory, consultez la rubrique parente de cette rubrique : [Active Directory des interfaces de service](active-directory-service-interfaces-adsi.md), ainsi que la rubrique sœur : [à propos des interfaces de service Active Directory](about-adsi.md).

 

Active Directory est une base de données à usage spécifique ; il ne s’agit pas d’un remplacement du Registre. Le répertoire est conçu pour gérer un grand nombre d’opérations de lecture et de recherche et un nombre nettement plus réduit de modifications et de mises à jour. Active Directory données sont hiérarchiques, répliquées et extensibles. Étant donné qu’il est répliqué, vous ne souhaitez pas stocker de données dynamiques, telles que les prix des actions d’entreprise ou les performances de l’UC. Si vos données sont spécifiques à l’ordinateur, stockez les données dans le registre. Les données de file d’attente d’impression, les données de contact utilisateur et les données de configuration réseau/ordinateur sont des exemples typiques de données stockées dans l’annuaire. La base de données Active Directory se compose d’objets et d’attributs. Les objets et les définitions d’attributs sont stockés dans le schéma Active Directory.

Vous vous demandez peut-être quels objets sont actuellement stockés dans Active Directory. Active Directory a trois partitions. Ils sont également connus sous le nom de contextes de nommage : domaine, schéma et configuration. La partition de domaine contient les utilisateurs, les groupes, les contacts, les ordinateurs, les unités d’organisation et de nombreux autres types d’objets. Étant donné que Active Directory est extensible, vous pouvez également ajouter vos propres classes et/ou attributs. La partition de schéma contient des classes et des définitions d’attributs. La partition de configuration comprend des données de configuration pour les services, les partitions et les sites.

La capture d’écran suivante montre la partition de domaine Active Directory.

![partition de domaine Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès Active Directory à l’aide de Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Scénario : Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 