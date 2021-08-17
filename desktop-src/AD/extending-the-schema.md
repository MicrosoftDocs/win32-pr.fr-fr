---
title: Extension du schéma
description: Le schéma de service Active Directory Directory définit les attributs et les classes utilisés dans Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, schéma, extension du schéma
- schéma AD, extension du schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189557"
---
# <a name="extending-the-schema"></a>Extension du schéma

Le schéma de service Active Directory Directory définit les attributs et les classes utilisés dans Active Directory Domain Services. Le schéma de base inclus dans le système contient un ensemble complet de définitions de classe, telles que **User**, **Computer** et **OrganizationalUnit**, ainsi que des définitions d’attributs, telles que **userPrincipalName**, **telephoneNumber** et **objectSID**. L’ensemble existant de classes et d’attributs sera suffisant pour la plupart des applications. Toutefois, le schéma est extensible, ce qui signifie que vous pouvez définir de nouvelles classes et attributs. Cette section explique comment étendre le schéma Active Directory.

## <a name="when-to-extend-the-schema"></a>Quand étendre le schéma

Si les classes et les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous devez étendre le schéma. Il est important de noter que les ajouts de schéma sont permanents ; vous pouvez désactiver des classes et des attributs, mais vous ne pouvez jamais les supprimer du schéma. Gardez cela à l’esprit lorsque vous testez du code.

Tenez également compte de la taille des données que vous souhaitez stocker. Microsoft recommande qu’aucune valeur d’attribut ne dépasse 500 kilo-octets, y compris la somme des attributs à valeurs multiples. En outre, la taille des objets ne doit pas dépasser 1 Mo. Tenez également compte du nombre d’instances des données ; Si vous ajoutez un nouvel attribut à la classe [**utilisateur**](/windows/desktop/ADSchema/c-user) sur un système qui a 100 000 utilisateurs, cela peut consommer un espace considérable.

Les rubriques de cette section sont les suivantes :

-   Comment effectuer une liaison au conteneur de schéma et lire les propriétés des classes et attributs existants.
-   Comment et quand étendre le schéma en définissant de nouveaux attributs et classes.
-   Comment installer des extensions de schéma à l’aide de LDIFDE, CSVDE ou par programmation avec ADSI.

Pour plus d’informations et pour obtenir une vue d’ensemble du schéma Active Directory, y compris des informations sur l’implémentation de schéma, les définitions de classe et les définitions d’attributs, consultez [Active Directory schéma](active-directory-schema.md).

Pour plus d’informations, notamment des pages de référence pour les classes de schéma prédéfinies, les attributs et les syntaxes d’attribut, consultez la référence de schéma Active Directory dans la [référence de Active Directory Domain Services](active-directory-domain-services-reference.md).

 

 