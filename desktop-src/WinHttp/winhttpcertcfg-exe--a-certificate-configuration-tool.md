---
description: l’outil de configuration de certificat WinHTTP (Microsoft Windows HTTP Services), &\# 0034 ; WinHttpCertCfg.exe&\# 0034 ;, permet aux administrateurs d’installer et de configurer des certificats clients dans n’importe quel magasin de certificats accessible par le compte IWAM (Internet Server Web Application Manager). L’outil élimine également la nécessité d’effectuer des opérations spéciales pour les comptes, tels que le compte IWAM, pour accéder à des certificats lors de l’utilisation de pages d’Active Server (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, un outil de configuration de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b8fbfadd6cf0282f63b26c8dd40d5ef96b5f54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466426"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, un outil de configuration de certificat

l’outil de configuration de certificat [WinHTTP (Microsoft Windows HTTP Services)](about-winhttp.md) , « WinHttpCertCfg.exe », permet aux administrateurs d’installer et de configurer des certificats clients dans n’importe quel [*magasin de certificats*](glossary.md) accessible par le compte IWAM (internet Server Web Application Manager). L’outil élimine également la nécessité d’effectuer des opérations spéciales pour les comptes, tels que le compte IWAM, pour accéder à des certificats lors de l’utilisation de pages d’Active Server (ASP).

La console MMC (Microsoft Management Console) permet aux administrateurs d’importer des certificats client sur un ordinateur local. Toutefois, l’importation d’un certificat n’accorde pas automatiquement l’accès à la clé privée pour d’autres comptes. Cette clé privée est requise pour l’authentification par certificat client. l’outil de configuration de certificat WinHTTP (Microsoft Windows HTTP Services) vous permet d’accorder l’accès à des comptes supplémentaires, tels que le compte IWAM, si nécessaire.

-   [Utilisation de l’outil de configuration de certificat](#using-the-certificate-configuration-tool)
-   [Exemples](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Utilisation de l’outil de configuration de certificat

l’outil de configuration de certificat WinHTTP, WinHttpCertCfg.exe, est disponible en téléchargement sur le site web des [outils du Kit de ressources Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . L’exemple de code suivant montre les paramètres de ligne de commande valides à utiliser avec cet outil.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

Le tableau suivant répertorie les paramètres de l’outil de configuration de.




| Paramètre | Description | 
|-----------|-------------|
| -? | Affiche les données de syntaxe. | 
| -i | spécifie que le certificat doit être importé à partir d’un fichier de Exchange d’informations personnelles (PFX). Ce paramètre doit être suivi du nom du fichier. Lorsque ce paramètre est spécifié, les paramètres « -a » et « -c » doivent également être spécifiés. | 
| -g | Spécifie que l’accès est accordé à une clé privée. Lorsque ce paramètre est spécifié, les paramètres « -a », « -c » et « -s » doivent également être spécifiés. | 
| -r | Spécifie que l’accès est supprimé pour une clé privée. Lorsque ce paramètre est spécifié, les paramètres « -a », « -c » et « -s » doivent également être spécifiés. | 
| -l | Spécifie que les comptes ayant accès à une clé privée sont répertoriés. Lorsque ce paramètre est spécifié, les paramètres « -c » et « -s » doivent également être spécifiés. | 
| -a | Spécifie le compte d’utilisateur sur l’ordinateur en cours de configuration. Il peut s’agir d’un ordinateur local ou d’un compte de domaine, tel que « IWAM_TESTMACHINE », « UTILISATEURTEST » ou « TESTDOMAIN\DOMAINUSER ». | 
| -c | Spécifie l’emplacement et le nom du <a href="glossary.md"><em>magasin de certificats</em></a>. Utilisez « LOCAL_MACHINE » ou « CURRENT_USER » pour désigner la branche du Registre à utiliser pour l’emplacement. Le <em>magasin de certificats</em> peut être installé sur l’ordinateur. Les exemples de noms standard sont « MY », « root » et « TrustedPeople ». L’emplacement et le nom du <em>magasin de certificats</em> sont séparés par une barre oblique inverse, par exemple, « LOCAL_MACHINE \Root ».<blockquote>[!Note]<br />Bien que la branche « CURRENT_USER » du Registre puisse être spécifiée avec ce paramètre, l’extension de l’accès aux clés privées est principalement destinée aux certificats installés dans un <a href="glossary.md"><em>magasin de certificats</em></a> d’ordinateur local accessible par plusieurs utilisateurs.</blockquote><br /> | 
| -S | Spécifie une chaîne de recherche ne respectant pas la casse pour rechercher le premier certificat énuméré avec un nom d’objet qui contient cette sous-chaîne. | 
| -p | Spécifie un mot de passe utilisé pour importer le certificat et la clé privée. Utilisé uniquement avec l’option d’importation. | 




 

> [!NOTE]
> L’utilisateur doit disposer des privilèges suffisants pour utiliser cet outil, ce qui nécessite que l’utilisateur soit un administrateur et le même utilisateur qui a installé le certificat client, s’il est installé.
>
> L’outil « WinHttpCertCfg.exe » n’est pas utile pour configurer des certificats stockés dans un système de fichiers tel que FAT32, qui ne prend pas en charge les listes de contrôle d’accès (ACL).

## <a name="examples"></a>Exemples

Les exemples suivants illustrent quelques-unes des façons dont l’outil de configuration peut être utilisé.

1.  Cette commande répertorie les comptes qui ont accès à la clé privée pour le certificat « MyCertificate » dans le [*magasin de certificats*](glossary.md) « racine » de la \_ branche de l’ordinateur local du Registre.

    **WinHttpCertCfg-l-c \_ racine de l’ordinateur local \\ -s MyCertificate**

2.  Cette commande accorde l’accès à la clé privée du certificat « MyCertificate » dans le [*magasin de certificats*](glossary.md) « My » pour le compte Utilisateurtest.

    **WinHttpCertCfg-g-c \_ machine locale \\ My-s MyCertificate-a TESTUSER**

3.  Cette commande importe un certificat et une clé privée à partir d’un fichier PFX et étend l’accès à la clé privée à un autre compte.

    **WinHttpCertCfg-i PFXFile-c \_ ordinateur local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**

4.  Cette commande refuse l’accès à la clé privée pour le \_ compte IWAM TESTMACHINE avec le certificat spécifié.

    **WinHttpCertCfg-r-c \_ racine de l’ordinateur local \\ -s MyCertificate-a IWAM \_ TESTMACHINE**

 

 




