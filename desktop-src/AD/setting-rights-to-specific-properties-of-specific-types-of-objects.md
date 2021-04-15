---
title: Définition de droits sur des propriétés spécifiques de types spécifiques d’objets
description: Les autorisations spécifiques à une propriété peuvent être utilisées en association avec l’héritage spécifique à l’objet pour fournir la délégation d’administration puissante et détaillée.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- définition de droits sur des propriétés spécifiques de types spécifiques d’objets Active Directory
- Active Directory, utilisation de, sécurité, définition de droits sur des propriétés spécifiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462815"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Définition de droits sur des propriétés spécifiques de types spécifiques d’objets

Les autorisations spécifiques à une propriété peuvent être utilisées en association avec l’héritage spécifique à l’objet pour fournir la délégation d’administration puissante et détaillée. Vous pouvez définir une entrée de contrôle d’accès héritable d’un objet spécifique à une propriété pour permettre à un utilisateur ou un groupe spécifié de lire et/ou d’écrire un attribut spécifique sur une classe spécifiée d’objets enfants dans un conteneur. Par exemple, vous pouvez définir une entrée du contrôle d’accès sur une unité d’organisation pour permettre à un groupe de lire et d’écrire l’attribut de numéro de téléphone de tous les objets utilisateur dans l’unité d’organisation.

**Pour définir des ACE qui héritent d’un objet spécifique aux propriétés**

1.  Définissez [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.
2.  Définissez [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **schemaIDGUID** de l’attribut. Par exemple, le **schemaIDGUID** de l’attribut **telephoneNumber** est {bf967a49-0de6-11D0-A285-00aa003049e2}.
3.  Définir [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ ACEFLAG \_ hériter \_** de l’entrée du contrôle d’accès.
4.  Définissez [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **schemaIDGUID** de la classe d’objet qui peut hériter de l’entrée du contrôle d’accès. Par exemple, le **schemaIDGUID** de la classe d' **utilisateur** est {bf967aba-0de6-11D0-A285-00aa003049e2}.
5.  Définissez [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **\_ type d’objet indicateur ADS \_ \_ \_ présent** et le **type d' \_ objet hérité de l’indicateur ADS est \_ \_ \_ \_ présent**.

> [!IMPORTANT]
> Définissez ad \_ ACEFLAG \_ inherit \_ ACE pour que l’entrée du contrôle d’accès soit héritée. En outre, Set ad \_ ACEFLAG \_ inherit \_ only \_ ACE si le type d’objet auquel s’applique cette entrée du contrôle d’accès ne correspond pas au type d’objet du conteneur dans lequel l’entrée du contrôle d’accès est spécifiée. Si ce n’est pas le cas, l’entrée du contrôle d’accès prendra également effet sur le conteneur et peut accorder des droits inattendus.

 

Pour plus d’informations et d’exemples de code qui peuvent être utilisés pour définir ce type d’entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée](example-code-for-setting-an-ace-on-a-directory-object.md)du contrôle d’accès sur un objet d’annuaire.

 

 