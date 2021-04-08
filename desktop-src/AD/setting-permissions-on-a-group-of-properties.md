---
title: Définition des autorisations sur un groupe de propriétés
description: Les autorisations peuvent être appliquées à un groupe de propriétés.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Définition des autorisations sur un groupe de propriétés Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724412"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Définition des autorisations sur un groupe de propriétés

Les autorisations peuvent être appliquées à un groupe de propriétés. Un jeu de propriétés est identifié par le GUID dans l’attribut [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) d’un objet [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) . Ce GUID est défini dans l’attribut [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) de l’objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de chaque attribut du groupe.

La procédure suivante montre comment définir des autorisations qui s’appliquent à un groupe de propriétés d’objet.

**Pour définir des autorisations qui s’appliquent à un groupe de propriétés d’objet**

1.  Affectez à la propriété [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) la valeur **ADS \_ Right \_ \_ lire \_ prop**, active **\_ \_ Directory Right \_ Write \_ prop** ou les deux valeurs combinées.
2.  Affectez à la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) la valeur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.
3.  Définissez la propriété [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le GUID du jeu de propriétés. Il s’agit de la propriété [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) de l’objet [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) qui identifie le jeu de propriétés. Ce GUID est également défini en tant que [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) dans l’objet attributeSchema de chaque propriété du groupe.
4.  Définissez la propriété [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **type d' \_ objet indicateur ADS \_ \_ \_ présent**.

N’oubliez pas que vous ne devez pas définir l’indicateur d' **accès au contrôle de \_ service d' \_ annuaire \_ \_ ad Right** dans la propriété [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) . Cet indicateur est utilisé uniquement pour spécifier un droit d’accès de contrôle.

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir les droits d’accès d’un jeu de propriétés, consultez [exemple de code pour la définition d’autorisations sur un groupe de propriétés](example-code-for-setting-permissions-on-a-group-of-properties.md).

Pour plus d’informations sur la création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès pour un jeu de propriétés, consultez [exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 