---
title: Access Control et création d’objets
description: Le serveur Active Directory ne parvient pas à créer un objet enfant si l’appelant ne dispose pas de l' \_ enfant ad droit \_ créer un \_ \_ enfant pour ce type d’objet sur le conteneur parent.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- PUBLICITÉ pour la création de Access Control et d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101400"
---
# <a name="access-control-and-object-creation"></a>Access Control et création d’objets

Le serveur Active Directory ne parvient pas à créer un objet enfant si l’appelant ne dispose pas de l' **\_ enfant ad droit \_ créer un \_ \_ enfant** pour ce type d’objet sur le conteneur parent. Pour déterminer les types d’objets enfants que l’appelant peut créer dans un objet d’annuaire, lisez l’attribut **allowedChildClassesEffective** de l’objet.

Quand vous utilisez la méthode [**IADsContainer :: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour créer un objet enfant, l’objet n’est pas rendu persistant tant que [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) n’est pas appelé sur le nouvel objet. Entre les appels **Create** et **setinfo** , le thread de création peut placer des valeurs dans n’importe laquelle des propriétés de l’objet. Après l’appel de **setinfo** , le thread de création ne dispose pas nécessairement des droits d’accès nécessaires pour définir les propriétés du nouvel objet. Pour vous assurer que l’appelant dispose de ces droits, spécifiez un descripteur de sécurité explicite lors de la création. La liste DACL doit avoir un ACE qui donne à l’appelant les droits d’accès nécessaires sur l’objet.

Pour plus d’informations sur le contrôle d’accès et la création d’objets, consultez [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 