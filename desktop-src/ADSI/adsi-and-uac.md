---
title: Contrôle de compte d’utilisateur et ADSI
description: Windows et Windows serveur possèdent un contrôle de compte d’utilisateur, qui a des ramifications pour les applications qui utilisent les Interfaces de Service de Active Directory (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1d0163348356f83b64522c9b05607d0d094ceb8f0ad530a798e546021433ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023967"
---
# <a name="adsi-and-user-account-control"></a>Contrôle de compte d’utilisateur et ADSI

Windows et Windows serveur possèdent un [contrôle de compte d’utilisateur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), qui a des ramifications pour les applications qui utilisent les Interfaces de Service de [Active Directory](active-directory-service-interfaces-adsi.md) (ADSI). Plus précisément, ces interfaces ont été conçues pour être exécutées par un compte d’utilisateur disposant de privilèges d’administrateur sur l’ordinateur local.

**Problème**

Chaque fois qu’une application se connecte à l’annuaire et tente de créer un objet ADSI, les modifications sont recherchées dans le [schéma de Active Directory](/windows/desktop/ADSchema/active-directory-schema) . Si elle a changé depuis la dernière connexion, le schéma est téléchargé et stocké dans un cache sur l’ordinateur local. dans les versions de Windows antérieures à Windows Vista, l’emplacement par défaut de ce cache était

`%systemroot%\SchCache\`

Toutefois, les applications exécutées par les comptes standard (c’est-à-dire non-administrateur) n’ont pas accès à ce répertoire. par conséquent, les applications qui utilisent des interfaces ADSI qui sont exécutées dans ce mode téléchargent le schéma à chaque connexion, ce qui aura un impact sur le débit et les performances.

**Solutions**

*Utilisateur unique* : pour résoudre ce problème, il existe de nouvelles clés de contrôle de Registre du fournisseur ADSI qui déterminent les emplacements de Registre et les emplacements de fichiers pour les objets de [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) mis en cache. Si la clé de Registre

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

a la valeur 0 (zéro), chaque utilisateur aura un emplacement de stockage différent pour ADSI ; les clés de Registre seront stockées dans

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

et les fichiers cache sont stockés dans

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

ces paramètres sont les paramètres par défaut sur les ordinateurs exécutant Windows Server 2008 ou Windows Vista.

*Multi-utilisateur* : Si vous exécutez des applications ADSI sur un ordinateur avec de nombreux comptes d’utilisateur (par exemple, un serveur Web), il est préférable de ne pas avoir de nombreuses copies du cache du [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) à l’aide d’une grande quantité d’espace disque. Définition de la clé de Registre

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

la valeur 1 (un) restaure le comportement précédent de l’interface ADSI. tous les objets de [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) seront stockés dans leurs emplacements précédents. la clé de Registre se trouve dans

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

et le fichier cache se trouve dans

`%systemroot%\SchCache`

Dans ce cas, les comptes d’administrateur doivent exécuter l’application, ce qui entraîne la mise en cache du fichier de schéma dans l’emplacement global pour une utilisation ultérieure par les utilisateurs moins privilégiés.

 

 