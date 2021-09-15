---
description: Liste des ressources protégées
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Liste des ressources protégées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521901"
---
# <a name="protected-resource-list"></a>Liste des ressources protégées

L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller. les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des Modules Windows.

WRP protège les fichiers avec les extensions suivantes qui sont installées par Windows Server 2008 ou Windows Vista : .dll, .exe,. ocx et .sys.

WRP protège les fichiers critiques installés par Windows Server 2008 ou Windows Vista avec les extensions suivantes :. acm,. ade,. adp,. app,. asa,. asp,. aspx,. ax,. bas, .bat,. bin,. cer,. chm,. clb,. cmd,. cnt,. cnv,. com, .cpl,. cpx,. crt,. csh, .dll,. drv,. dtd, .exe,. fxp,. grp,. h1s,. hlp,. hta,. ime,. inf,. ins,. isp,. its, .js,. jse,. ksh,. lnk,. mad,. maf,. mag,. gam,. man,. maq,. mar,. mas,. mat,. mau,. pif,. maw,. mda,. mdb,. mde,. mdt,. mdw,. mdz,. msc, .msi,. msp,. mst,. mui,. nls,. ocx,. ops,. pal,. pcd,. pif,. prf,. prg,. pst,. reg,. scf,. scr,. sct,. shb,. shs, .sys,. tlb,. tsp,. url,. vb,. vbe,. vbs,. vsmacros,. vss,. vst,.,. ws,. wsc,. wsf,. wsh,  . xsd et. Xsl.

WRP protège les dossiers critiques. un dossier contenant uniquement des fichiers protégés par WRP peut être verrouillé afin que seul le Windows programme d’installation approuvé puisse créer des fichiers ou des sous-dossiers dans le dossier. Un dossier peut être partiellement verrouillé pour permettre aux administrateurs de créer des fichiers et des sous-dossiers dans le dossier.

WRP protège les clés de registre essentielles installées par Windows Server 2008 et Windows Vista. Si une clé est protégée par WRP, toutes ses sous-clés et valeurs peuvent être protégées.

WRP copie les fichiers nécessaires pour redémarrer Windows dans le *répertoire de cache* situé à la sauvegarde% Windir% \\ winsxs \\ . les fichiers critiques qui ne sont pas nécessaires pour redémarrer Windows ne sont pas copiés dans le répertoire du cache. La taille du répertoire du cache et la liste des fichiers copiés dans le cache ne peuvent pas être modifiées.

* * Windows Server 2003 et Windows XP : * *

Windows Protection de fichiers (WFP) précédée de WRP.

WFP protège les fichiers installés par Windows avec les extensions suivantes : .dll, .exe,. ocx et .sys. En outre, les polices TrueType. ttf, Tahoma. ttf et tahomabd. ttf sont également protégées.

à la fin de l’installation de Windows, WFP exécute une analyse de tous les fichiers protégés pour s’assurer qu’ils n’ont pas été modifiés par les applications installées par le biais d’une installation sans assistance. WFP copie également les versions vérifiées de ces fichiers système dans le répertoire du cache. Lorsqu’une application tente de remplacer un fichier protégé, WFP peut restaurer le fichier d’origine à partir du répertoire du cache.

La valeur par défaut est% SystemRoot% \\ system32 \\ dllcache. pour spécifier un autre emplacement pour le cache, créez la valeur de registre suivante : **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Il doit s’agir d’un chemin d’accès local. L’utilisation d’un chemin d’accès réseau crée une seule source de réseau partagé pour les fichiers cache, à condition que tous les clients qui utilisent le partage exécutent les mêmes service packs et correctifs logiciels.

La taille par défaut du cache est illimitée. pour modifier la taille du cache, utilisez le paramètre de registre suivant : **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Si la valeur est le \_ quota SFC \_ tous les \_ fichiers, tous les fichiers système sont mis en cache dans le répertoire du cache.

En raison des considérations relatives à l’espace disque, il n’est pas souhaitable de conserver les versions mises en cache de tous les fichiers système dans le répertoire du cache. Selon la taille du cache, la protection des fichiers Windows stocke les versions de fichiers vérifiées dans le répertoire de cache du disque dur système. WFP ajoute des fichiers au cache jusqu’à ce que la taille du répertoire du cache atteigne la limite spécifiée.

Lorsqu’une application tente de remplacer un fichier protégé qui ne se trouve pas dans le cache, WFP tente de restaurer le fichier d’origine à partir de la source d’installation, en invitant l’utilisateur si nécessaire.

 

 



