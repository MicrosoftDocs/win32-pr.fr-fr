---
description: Lorsque vous vous connectez à distance à un serveur Active Directory autre que celui qui se trouve dans votre domaine actuel, vous devez spécifier le nom d’un ordinateur qui est déjà membre du domaine appartenant au Active Directory souhaité.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Description de l’espace de noms LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad19ea98e5bd6f36ff78159bfe0a106f0772921c152aa167c38e435732188446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568619"
---
# <a name="describing-the-ldap-namespace"></a>Description de l’espace de noms LDAP

Lorsque vous vous connectez à distance à un serveur Active Directory autre que celui qui se trouve dans votre domaine actuel, vous devez spécifier le nom d’un ordinateur qui est déjà membre du domaine appartenant au Active Directory souhaité.

Pour vous connecter à distance à un ordinateur qui est déjà membre du domaine appartenant au serveur Active Directory, tapez la commande suivante.

**\\\\\\ \\ Protocole LDAP de répertoire racine ordinateur_distant \\**

Cet exemple montre que deux parties composent un nom d’espace de noms qualifié complet. La première partie ( \\ \\ ordinateur_distant) représente l’ordinateur qui est déjà membre du domaine appartenant au serveur Active Directory de votre choix. La deuxième partie ( \\ \\ répertoire racine \\ LDAP) représente le schéma Active Directory dans le fournisseur de services d’annuaire.

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

 

 



