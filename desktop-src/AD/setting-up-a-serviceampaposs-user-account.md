---
title: Configuration du compte d’utilisateur d’un service
description: Votre programme d’installation de service peut suggérer un compte d’ouverture de session par défaut pour une instance de service et permettre à l’administrateur de sélectionner le compte par défaut ou d’en spécifier un autre.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Configuration de l’AD du compte d’utilisateur d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724405"
---
# <a name="setting-up-a-services-user-account"></a>Configuration du compte d’utilisateur d’un service

Votre programme d’installation de service peut suggérer un compte d’ouverture de session par défaut pour une instance de service et permettre à l’administrateur de sélectionner le compte par défaut ou d’en spécifier un autre. Si l’administrateur sélectionne un compte d’utilisateur, plutôt que le compte LocalSystem, le compte doit exister avant d’appeler la fonction [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) pour installer une instance du service sur un serveur hôte. Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour créer un nouvel objet utilisateur de domaine dans Active Directory Domain Services, consultez [création d’un utilisateur](creating-a-user.md).

Dans l’idéal, chaque instance d’un service, qu’il s’agisse d’un service basé sur l’hôte ou d’un service réplicable, doit avoir son propre compte d’utilisateur de domaine. L’utilisation de comptes distincts pour chaque instance de service est plus sécurisée que si plusieurs instances partagent le même compte. En outre, l’utilisation de comptes distincts permet d’auditer les activités de chaque instance de service.

Lorsque votre programme d’installation suggère un compte d’ouverture de session par défaut, il doit spécifier le nom d’un nouveau compte à créer pour la nouvelle instance de service. Le nom du compte peut être composé des mêmes éléments que ceux utilisés pour composer un nom de principal du service, tel que la classe de service, l’ordinateur hôte et le nom de service. Pour plus d'informations, consultez la page [Noms de principal de service](service-principal-names.md). En règle générale, vous créez le compte dans le conteneur utilisateurs sur le domaine de l’ordinateur hôte.

Vous devez générer un mot de passe pour chaque compte. Pour plus d’informations sur l’écriture d’un outil qui automatise la tâche de mise à jour des mots de passe de compte de service, consultez [modification du mot de passe sur le compte d’utilisateur d’un service](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 