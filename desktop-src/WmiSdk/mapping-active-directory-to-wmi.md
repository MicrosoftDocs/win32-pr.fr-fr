---
description: Le fournisseur de services d’annuaire met en miroir des classes et des instances de Active Directory dans l’espace de noms LDAP (Lightweight Directory Access Protocol) WMI.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Mappage de Active Directory à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918791"
---
# <a name="mapping-active-directory-to-wmi"></a>Mappage de Active Directory à WMI

Le fournisseur de services d’annuaire met en miroir des classes et des instances de Active Directory dans l’espace de noms LDAP (Lightweight Directory Access Protocol) WMI. En raison des différences fondamentales dans les deux environnements, vous ne pouvez pas simplement renommer les classes et les instances de Active Directory et espérons qu’elles accèdent correctement à ces classes et instances dans WMI. Au lieu de cela, le fournisseur de services d’annuaire suit des règles d’affectation de noms pour conserver les relations qui existent entre les classes Active Directory et les instances.

Les rubriques suivantes fournissent des informations sur le mappage des classes et des instances de Active Directory :

-   [Mapper des classes Active Directory](mapping-active-directory-classes.md)
-   [Mappage d’instances Active Directory](mapping-active-directory-instances.md)

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

 

 



