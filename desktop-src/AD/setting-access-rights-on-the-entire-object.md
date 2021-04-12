---
title: Définition des droits d’accès sur l’objet entier
description: Certaines autorisations peuvent être définies uniquement pour un objet entier, par exemple supprimer et répertorier le contenu. Les autorisations spécifiques à l’opération, telles que l’autorisation lecture, peuvent également être définies pour l’ensemble de l’objet afin qu’elles s’appliquent à un objet entier.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Définition des droits d’accès sur l’ensemble de l’objet AD
- objets AD, définition des droits d’accès sur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462818"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Définition des droits d’accès sur l’objet entier

Certaines autorisations peuvent être définies uniquement pour un objet entier, par exemple supprimer et répertorier le contenu. Les autorisations spécifiques à l’opération, telles que l’autorisation lecture, peuvent également être définies pour l’ensemble de l’objet afin qu’elles s’appliquent à un objet entier.

La procédure suivante peut être utilisée pour définir des autorisations pour un objet entier.

**Pour définir des autorisations pour un objet entier**

1.  Définissez [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ accès \_ autorisé** ou **ad \_ AceType \_ accès \_ refusé**.
2.  Affectez à [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) et **IADsAccessControlEntry. InheritedObjectType** la valeur **null**.

Pour plus d’informations sur la création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 