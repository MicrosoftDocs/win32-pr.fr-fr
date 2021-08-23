---
title: Définition d’une entrée de contrôle d’accès de droit de contrôle dans l’ACL d’un objet
description: À l’aide d’ADSI, vous définissez un ACE droit d’accès au contrôle comme vous le feriez pour une entrée de contrôle d’accès spécifique à la propriété, à la différence près que la propriété IADsAccessControlEntry. ObjectType est le rightsGUID du droit d’accès du contrôle.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Définition d’une entrée de contrôle d’accès de droit de contrôle dans l’ACL d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024807"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Définition d’une entrée de contrôle d’accès de droit de contrôle dans l’ACL d’un objet

À l’aide d’ADSI, vous définissez un ACE droit d’accès au contrôle comme vous le feriez pour une entrée de contrôle d’accès spécifique à la propriété, à la différence près que la propriété [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) est le **rightsGUID** du droit d’accès du contrôle. N’oubliez pas que vous pouvez également utiliser les API de sécurité Win32 pour définir des listes de contrôle d’accès sur des objets d’annuaire.

Le tableau suivant répertorie les propriétés [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour les droits d’accès de contrôle qui peuvent être utilisés pour définir les propriétés d’une entrée du contrôle d’accès.



| Propriété                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Pour les droits d’accès de contrôle qui contrôlent l’accès aux droits étendus à des opérations spéciales, AccessMask doit contenir l’indicateur d' **\_ \_ \_ \_ accès au contrôle DS droit ADS** . Pour les droits d’accès de contrôle qui définissent un jeu de propriétés, AccessMask contient les **publicités \_ Right \_ DS \_ Read \_ prop** et/ou active **\_ \_ Directory Right \_ Write \_ prop**.<br/> Pour les droits d’accès de contrôle qui contrôlent les écritures validées, [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contient les **annonces \_ \_ DS \_ Self**.<br/> |
| [**Indicateurs**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Cette valeur doit inclure l’indicateur de **\_ type d’objet indicateur ADS \_ \_ \_ présent** .                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Cette valeur doit être le format [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) de l’attribut **rightsGUID** du droit d’accès de contrôle. Sachez que, dans une entrée du contrôle d’accès, la chaîne GUID doit inclure les accolades de début et de fin, même si l’attribut **rightsGUID** de l’objet **controlAccessRight** n’inclut pas les accolades.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | **Ad \_ ACETYPE \_ Access \_ allowed \_ Object autorisé** à accorder au tiers de confiance le droit de contrôle d’accès ou l' **\_ objet ad ACETYPE \_ Access \_ denied \_** pour refuser au tiers de confiance le droit d’accès au contrôle.                                                                                                                                                                                                                                                                                                     |
| [**Tiers**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Principal de sécurité, par exemple utilisateur, groupe, ordinateur, et ainsi de suite, auquel s’applique l’entrée du contrôle d’accès.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Pour plus d’informations sur la création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour plus d’informations et pour obtenir un exemple de code pour définir une entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

 

