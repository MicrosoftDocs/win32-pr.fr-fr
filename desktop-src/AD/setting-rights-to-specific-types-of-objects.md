---
title: Définition de droits sur des types d’objets spécifiques
description: La procédure suivante montre comment définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- définition de droits sur les types d’objets AD
- objets AD, définition de droits sur
- Active Directory, utilisation de, sécurité, définition de droits sur des types d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d8740b4454eac5de158c826ec135a0becf6777f320e16729598187a3093f088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183287"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Définition de droits sur des types d’objets spécifiques

La procédure suivante montre comment définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique.

 **Pour définir une entrée du contrôle d’accès qui peut être héritée uniquement par une classe d’objets spécifique**

1.  Définissez la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.
2.  Définissez la propriété [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de façon à inclure \_ l' \_ indicateur ACE inherit ACEFLAG de publicités \_ .
3.  Définissez la propriété [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **schemaIDGUID** de la classe d’objet qui peut hériter de l’entrée du contrôle d’accès.
4.  Définissez la propriété [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **type d' \_ objet hérité d’indicateur ADS \_ \_ \_ présent**.

> [!IMPORTANT]
> Définissez **ad \_ ACEFLAG \_ inherit \_ ACE** pour que l’entrée du contrôle d’accès soit héritée. En outre, vous devez définir les **publicités \_ ACEFLAG hériter de l' \_ \_ \_ ACE uniquement** si le type d’objet auquel s’applique cette entrée du contrôle d’accès ne correspond pas au type d’objet du conteneur dans lequel l’entrée du contrôle d’accès est spécifiée. Si ce n’est pas le cas, l’entrée du contrôle d’accès prendra également effet sur le conteneur et peut accorder des droits inattendus.

 

Pour plus d’informations et d’exemples de code qui peuvent être utilisés pour définir ce type d’entrée du contrôle d’accès, consultez [exemple de code pour la définition d’une entrée](example-code-for-setting-an-ace-on-a-directory-object.md)du contrôle d’accès sur un objet d’annuaire.

 

 