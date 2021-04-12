---
title: Droits d’accès au contrôle (AD DS)
description: Tous les objets de Active Directory Domain Services prennent en charge un jeu standard de droits d’accès défini dans l’énumération d’énumération des \_ droits ADS \_ .
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Contrôler les droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c4aa685e0c569ef2ac762dcf17366a2394826
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462907"
---
# <a name="control-access-rights-ad-ds"></a>Droits d’accès au contrôle (AD DS)

Tous les objets de Active Directory Domain Services prennent en charge un jeu standard de droits d’accès défini dans l’énumération d’énumération des [**\_ \_ droits ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) . Ces droits d’accès peuvent être utilisés dans les entrées du Access Control (ACE) du descripteur de sécurité d’un objet pour contrôler l’accès à l’objet. autrement dit, pour contrôler qui peut effectuer des opérations standard, telles que la création et la suppression d’objets enfants, ou la lecture et l’écriture des attributs d’objet. Toutefois, pour certaines classes d’objets, il peut être souhaitable de contrôler l’accès d’une manière non prise en charge par les droits d’accès standard. Pour faciliter cette tâche, Active Directory Domain Services autoriser l’extension du mécanisme de contrôle d’accès standard par le biais de l’objet **controlAccessRight** .

Les droits de contrôle d’accès sont utilisés de trois façons :

-   Pour les droits étendus, qui sont des opérations spéciales non couvertes par le jeu standard de droits d’accès. Par exemple, la classe d’utilisateur peut recevoir un droit « envoyer en tant que » qui peut être utilisé par Exchange, Outlook ou toute autre application de messagerie pour déterminer si un utilisateur particulier peut demander à un autre utilisateur d’envoyer un courrier en son nom. Les droits étendus sont créés sur les objets **controlAccessRight** en affectant à l’attribut **validAccesses** la valeur égal au droit d’accès au **contrôle d' \_ \_ \_ \_ accès au service d’annuaire Active Directory** (256).
-   Pour la définition de jeux de propriétés, pour permettre le contrôle de l’accès à un sous-ensemble des attributs d’un objet, plutôt qu’uniquement aux attributs individuels. En utilisant les droits d’accès standard, une seule ACE peut accorder ou refuser l’accès à tous les attributs d’un objet ou à un attribut unique. Les droits de contrôle d’accès permettent à une seule entrée de contrôle d’accès de contrôler l’accès à un ensemble d’attributs. Par exemple, la classe utilisateur prend en charge le jeu de propriétés **informations personnelles** qui comprend des attributs tels que adresse postale et numéro de téléphone. Les droits de jeu de propriétés sont créés sur les objets **controlAccessRight** en définissant l’attribut **validAccesses** pour qu’il contienne à la fois les droits d’accès **ACTR \_ DS \_ Read \_ prop** (16) et **ACTRL \_ DS \_ Write \_ prop** (32).
-   Pour les écritures validées, pour exiger que le système effectue la vérification de la valeur, ou la validation, au-delà de ce qui est requis par le schéma, avant d’écrire une valeur dans un attribut sur un objet de service d’annuaire. Cela permet de s’assurer que la valeur entrée pour l’attribut est conforme à la sémantique requise, qu’elle est comprise dans une plage de valeurs autorisées ou qu’elle subit d’autres vérifications spéciales qui ne seraient pas effectuées pour une simple écriture de bas niveau vers l’attribut. Une écriture validée est associée à une autorisation spéciale qui est distincte de l’autorisation « Write <attribute> » qui autorise l’écriture d’une valeur dans l’attribut sans vérification de la valeur. L’écriture validée est le seul l’un des trois droits d’accès de contrôle qui ne peut pas être créé en tant que nouveau droit d’accès de contrôle pour une application. Cela est dû au fait que le système existant ne peut pas être modifié par programmation pour appliquer la validation. Si un droit d’accès de contrôle a été configuré dans le système en tant qu’écriture validée, l’attribut **validAccesses** sur les objets **controlAccessRight** contient le droit d’accès **\_ \_ \_ Self DS Right** (8).

    Seules trois écritures validées sont définies dans le schéma de Active Directory Windows 2000 :

    -   Self-Membership autorisation sur un objet de groupe, ce qui permet d’ajouter ou de supprimer le compte de l’appelant, mais aucun autre compte, de l’appartenance à un groupe.
    -   Autorisation validée-DNS-Host-Name sur un objet ordinateur, ce qui permet de définir un attribut de nom d’hôte DNS conforme au nom d’ordinateur et au nom de domaine.
    -   Autorisation validée-SPN sur un objet ordinateur, qui autorise un attribut SPN conforme au nom d’hôte DNS de l’ordinateur à définir.

Pour plus de commodité, chaque droit d’accès de contrôle est représenté par un objet **controlAccessRight** dans le conteneur Extended-Rights de la partition de configuration, même si les jeux de propriétés et les écritures validées ne sont pas considérés comme des droits étendus. Étant donné que le conteneur de configuration est répliqué dans toute la forêt, les droits de contrôle sont propagés sur tous les domaines d’une forêt. Il existe un certain nombre de droits d’accès au contrôle prédéfinis, et bien sûr, des droits d’accès personnalisés peuvent également être définis.

Tous les droits d’accès au contrôle peuvent être affichés en tant qu’autorisations dans l’éditeur ACL.

Pour plus d’informations et pour obtenir un exemple de code C++ et Visual Basic qui définit une entrée du contrôle d’accès pour contrôler l’accès en lecture/écriture à un jeu de propriétés, consultez l' [exemple de code permettant de définir une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

Pour plus d’informations sur l’utilisation des droits de contrôle d’accès pour contrôler l’accès aux opérations spéciales, consultez :

-   [Création d’un droit d’accès au contrôle](creating-a-control-access-right.md)
-   [Définition d’une entrée de contrôle d’accès de droit de contrôle dans l’ACL d’un objet](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Vérification d’un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lecture d’un droit d’accès de contrôle défini dans l’ACL d’un objet](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 