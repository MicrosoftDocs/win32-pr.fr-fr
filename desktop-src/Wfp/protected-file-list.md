---
description: Liste des ressources protégées
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Liste des ressources protégées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210568"
---
# <a name="protected-resource-list"></a>Liste des ressources protégées

L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller. Les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des modules Windows.

WRP protège les fichiers avec les extensions suivantes qui sont installées par Windows Server 2008 ou Windows Vista :. dll,. exe,. ocx et. sys.

WRP protège les fichiers critiques installés par Windows Server 2008 ou Windows Vista avec les extensions suivantes :. ACM,. ade,. ADP,. app,. ASA,. asp,. aspx,. ax,. bas,. bat,. bin,. cer,. chm,. CLB,. cmd,. CNT,. cnv,. com,. cpl,. CPX,. CRT,. csh,. dll,. drv,. DTD,. exe,. FXP,. GRP,. H1S,. hlp,. hta,. IME,. inf,. ins,. ISP,. son,. js,. JSE,. ksh,. lnk,. Mad,. MAF,. mag ,. gam,. Man,. maq,. Mar,. Mas,. mat,. Mau,.,. Maw,. MDA,. mdb,. mde,. MDT,. mdw,. mdz,. msc,. msi,. msp,. MST,. multilingue,. nls,. ocx,. OPS,. PAL,. PCD,. pif,. PRF,. PRG,. pst,. reg,. SCF,. scr,. SCT,. SHB,. SHS,. sys,. tlb,. tsp,. URL,. vb,.,. vb,. vsmacros,,. VSS,. VST,. n,. WS,. WSC,. wsf,. WSH,. xsd et. Xsl.

WRP protège les dossiers critiques. Un dossier contenant uniquement des fichiers protégés par WRP peut être verrouillé afin que seul le programme d’installation approuvé de Windows puisse créer des fichiers ou des sous-dossiers dans le dossier. Un dossier peut être partiellement verrouillé pour permettre aux administrateurs de créer des fichiers et des sous-dossiers dans le dossier.

WRP protège les clés de Registre essentielles installées par Windows Server 2008 et Windows Vista. Si une clé est protégée par WRP, toutes ses sous-clés et valeurs peuvent être protégées.

WRP copie les fichiers nécessaires au redémarrage de Windows dans le *Répertoire de cache* situé à la sauvegarde% windir% \\ WinSxS \\ . Les fichiers critiques qui ne sont pas nécessaires pour redémarrer Windows ne sont pas copiés dans le répertoire du cache. La taille du répertoire du cache et la liste des fichiers copiés dans le cache ne peuvent pas être modifiées.

* * Windows Server 2003 et Windows XP : * *

Protection des fichiers Windows (WFP) précédée de WRP.

WFP protège les fichiers installés par Windows avec les extensions suivantes :. dll,. exe,. ocx et. sys. En outre, les polices TrueType. ttf, Tahoma. ttf et tahomabd. ttf sont également protégées.

À la fin de l’installation de Windows, WFP exécute une analyse de tous les fichiers protégés pour s’assurer qu’ils n’ont pas été modifiés par les applications installées par le biais d’une installation sans assistance. WFP copie également les versions vérifiées de ces fichiers système dans le répertoire du cache. Lorsqu’une application tente de remplacer un fichier protégé, WFP peut restaurer le fichier d’origine à partir du répertoire du cache.

La valeur par défaut est% SystemRoot% \\ system32 \\ dllcache. Pour spécifier un autre emplacement pour le cache, créez la valeur de Registre suivante : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Il doit s’agir d’un chemin d’accès local. L’utilisation d’un chemin d’accès réseau crée une seule source de réseau partagé pour les fichiers cache, à condition que tous les clients qui utilisent le partage exécutent les mêmes service packs et correctifs logiciels.

La taille par défaut du cache est illimitée. Pour modifier la taille du cache, utilisez le paramètre de Registre suivant : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Si la valeur est le \_ quota SFC \_ tous les \_ fichiers, tous les fichiers système sont mis en cache dans le répertoire du cache.

En raison des considérations relatives à l’espace disque, il n’est pas souhaitable de conserver les versions mises en cache de tous les fichiers système dans le répertoire du cache. Selon la taille du cache, la protection des fichiers Windows stocke les versions de fichiers vérifiées dans le répertoire de cache du disque dur système. WFP ajoute des fichiers au cache jusqu’à ce que la taille du répertoire du cache atteigne la limite spécifiée.

Lorsqu’une application tente de remplacer un fichier protégé qui ne se trouve pas dans le cache, WFP tente de restaurer le fichier d’origine à partir de la source d’installation, en invitant l’utilisateur si nécessaire.

 

 



