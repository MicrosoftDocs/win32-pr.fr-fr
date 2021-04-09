---
title: Définition des autorisations sur les opérations sur les objets enfants
description: Les autorisations, telles que créer un enfant et supprimer un enfant, peuvent également être accordées ou refusées pour des opérations sur tous les sous-objets ou sous-objets d’une classe spécifique.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Définition des autorisations sur les opérations sur les objets enfants AD
- objets AD, Child, définition d’autorisations sur les opérations d’objets enfants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101420"
---
# <a name="setting-permissions-on-child-object-operations"></a>Définition des autorisations sur les opérations sur les objets enfants

Les autorisations, telles que créer un enfant et supprimer un enfant, peuvent également être accordées ou refusées pour des opérations sur tous les sous-objets ou sous-objets d’une classe spécifique.

La procédure suivante peut être utilisée pour définir des autorisations pour un type de sous-objet spécifique.

**Pour définir des autorisations pour un type de sous-objet spécifique**

1.  Définissez la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.
2.  Définissez la propriété [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le GUID de la classe d’objet. Il s’agit de la propriété **schemaIDGUID** de l’objet classSchema qui définit la classe d’objets. Si la propriété **ObjectType** a la **valeur null**, l’entrée du contrôle d’accès s’applique aux sous-objets de n’importe quelle classe.
3.  Définissez la propriété [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **type d' \_ objet indicateur ADS \_ \_ \_ présent**.

Pour plus d’informations et pour connaître la procédure de création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée de contrôle d’accès qui contrôle les opérations d’objets enfants, consultez [l’exemple de code pour la définition d’une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 