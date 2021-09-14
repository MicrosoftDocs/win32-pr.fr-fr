---
title: Utilisation du schéma ADSI
description: Un schéma définit l’univers des objets stockés dans un répertoire.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Utilisation du schéma ADSI
- ADSI ADSI, utilisation, schéma ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922036"
---
# <a name="using-the-adsi-schema"></a>Utilisation du schéma ADSI

Un schéma définit l’univers des objets stockés dans un répertoire. Dans Active Directory, le schéma spécifie les attributs que peut avoir un objet de service d’annuaire. Il spécifie également la plage de valeurs et la syntaxe des attributs, et indique s’ils prennent en charge des valeurs uniques ou multiples. En résumé, le schéma est organisé par définitions de classe, définitions d’attributs et syntaxe d’attribut. ADSI fournit trois interfaces permettant de lire les données d’attribut, de classe et de syntaxe à partir d’un schéma : [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)et [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory utilise un ensemble d’objets de schéma pour fournir une gestion de schéma dynamiquement extensible. Pour plus d’informations sur un objet inconnu, recherchez ses objets de schéma associés. Pour créer une définition de classe ou étendre une définition de classe existante, vous pouvez créer ou étendre les objets de schéma appropriés. Les objets de schéma sont organisés dans le conteneur de schéma d’un répertoire donné. Pour accéder à une classe de schéma d’objet, utilisez la propriété [**IADs. Schema**](iads-property-methods.md) de l’objet pour obtenir la chaîne ADsPath et utilisez cette chaîne pour établir une liaison à une interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) sur la classe de schéma d’objet.

Pour déterminer les définitions d’attributs, autrement dit, la plage de valeurs, la syntaxe, et ainsi de suite, inspectez les objets d’attribut de schéma pour chaque propriété prise en charge par l’objet de service d’annuaire. Pour plus d’informations sur l’accès aux objets d’attribut de schéma, consultez [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI extrait les données de syntaxe en fonction des besoins et vous permet d’utiliser [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) pour identifier la syntaxe requise pour représenter les données d’objet.

Pour plus d’informations sur le schéma Active Directory, consultez [Active Directory schéma](/windows/desktop/AD/active-directory-schema). Pour obtenir des exemples de code à utiliser pour lire le conteneur de schéma, consultez [lecture du schéma](reading-the-schema.md).

 

 