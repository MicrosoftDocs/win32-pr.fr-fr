---
title: Sauvegarde et restauration d’un serveur Active Directory
description: Active Directory Domain Services fournir des fonctions pour sauvegarder et restaurer des données dans la base de données d’annuaire.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilisation, sauvegarde et restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724652"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Sauvegarde et restauration d’un serveur Active Directory

Active Directory Domain Services fournir des fonctions pour sauvegarder et restaurer des données dans la base de données d’annuaire. Cette section décrit comment [sauvegarder](backing-up-an-active-directory-server.md) et [restaurer](restoring-an-active-directory-server.md) un serveur Active Directory. Pour plus d’informations sur la sauvegarde d’un serveur Active Directory à l’aide des utilitaires fournis dans les systèmes d’exploitation Windows 2000 et Windows Server 2003, consultez le kit de ressources applicables, disponible sur le site Web Microsoft TechNet.

La sauvegarde d’un serveur de Active Directory doit être effectuée en ligne et doit être effectuée lors de l’installation du Active Directory Domain Services. Active Directory Domain Services reposent sur une base de données spéciale et exportent un ensemble de fonctions de sauvegarde qui fournissent l’interface de sauvegarde par programme. La sauvegarde ne prend pas en charge les sauvegardes incrémentielles. Une application de sauvegarde se lie à une DLL côté client locale avec des points d’entrée définis dans ntdsbcli. h.

La restauration d’un serveur Active Directory est toujours effectuée en mode hors connexion.

Bien que les rubriques de cette section décrivent uniquement comment sauvegarder et restaurer un serveur Active Directory, sachez que Windows 2000 et les systèmes d’exploitation Windows Server 2003 disposent de plusieurs composants « État du système » qui doivent être sauvegardés et restaurés ensemble. Ces composants d’État du système sont constitués des éléments suivants :

-   Fichiers de démarrage tels que Ntldr, Ntdetect, tous les fichiers protégés par SFP et la configuration du compteur de performances
-   Contrôleur domaine Active Directory
-   SysVol (contrôleur de domaine uniquement)
-   Serveur de certificats (CA uniquement)
-   Base de données de cluster (nœud de cluster uniquement)
-   Registre
-   Base de données d’inscription de classe COM+

L’état du système peut être sauvegardé dans n’importe quel ordre, mais la restauration de l’état du système doit se produire dans l’ordre suivant :

1.  Restaurez les fichiers de démarrage.
2.  Restaurez SysVol, le serveur de certificats, la base de données de cluster et la base de données d’inscription de classe COM+, le cas échéant.
3.  Restaurez le serveur de Active Directory.
4.  Restaurez le registre.

Pour plus d’informations sur la sauvegarde et la restauration des services de certificats, consultez [utilisation des fonctions de sauvegarde et de restauration des services de certificats](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Pour plus d’informations sur la sauvegarde et la restauration de Active Directory Domain Services, consultez :

-   [Considérations relatives à la sauvegarde Active Directory Domain Services](considerations-for-active-directory-domain-services-backup.md)
-   [Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
-   [Restauration d’un serveur Active Directory](restoring-an-active-directory-server.md)
-   [Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)

 

 