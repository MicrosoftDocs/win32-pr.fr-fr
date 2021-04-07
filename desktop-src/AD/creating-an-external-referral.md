---
title: Création d’une référence externe
description: Si un objet crossRef externe est créé et qu’un contrôleur de domaine l’utilise pour générer une référence, l’objet crossRef fournit deux éléments de données importants dans les propriétés suivantes.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- références externes Active Directory
- Active Directory exemples Active Directory, création d’une référence externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724589"
---
# <a name="creating-an-external-referral"></a>Création d’une référence externe

Si un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) externe est créé et qu’un contrôleur de domaine l’utilise pour générer une référence, l’objet **crossRef** fournit deux éléments de données importants dans les propriétés suivantes. Pour plus d’informations sur les situations où cela peut se produire, consultez la section précédente.



| Propriété                           | Description                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Spécifie le serveur ou le domaine qui peut fournir des données à partir du contexte d’appellation spécifié dans [**NCName**](/windows/desktop/ADSchema/a-ncname).                                           |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Spécifie le nom unique pour le domaine, le schéma ou le conteneur de configuration enraciné sur le serveur ou le domaine spécifié par [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot). |



 

Par exemple, si le serveur avec l’adresse DNS serv1.northwest.Fabrikam.com sert de contexte d’appellation racine à CN = MyContainer, OU = MyDOM, O = Fabrikam, définissez le [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) sur l’adresse DNS de ce serveur et le [**NCName**](/windows/desktop/ADSchema/a-ncname) sur le nom unique du domaine, du schéma ou du conteneur de configuration.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une référence externe, consultez l' [exemple de code pour la création d’un objet crossRef externe](example-code-for-creating-an-external-crossref-object.md).

 

 