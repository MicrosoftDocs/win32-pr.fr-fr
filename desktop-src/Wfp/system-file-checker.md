---
description: L’utilitaire Vérificateur des fichiers système, Sfc.exe, permet aux administrateurs d’analyser toutes les ressources protégées pour vérifier leurs versions.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Vérificateur des fichiers système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f751aa30c06dbff90b8d5221974236b45edf9f0f278c144f755568a0040f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330281"
---
# <a name="system-file-checker"></a>Vérificateur des fichiers système

L’utilitaire Vérificateur des fichiers système, Sfc.exe, permet aux administrateurs d’analyser toutes les ressources protégées pour vérifier leurs versions.

les fichiers essentiels pour redémarrer Windows qui ne correspondent pas à la version de Windows attendue peuvent être remplacés par les versions appropriées. Si un fichier est réparé, les données de registre correspondantes sont également réparées. les fichiers protégés non critiques pour le redémarrage Windows ne sont pas réparés.

## <a name="syntax"></a>Syntaxe

Voici la syntaxe de la ligne de commande pour SFC.

**Options SFC \[ = chemin d’accès complet au fichier\]**

## <a name="options"></a>Options

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*
</dt> <dd>

Cette valeur n’est pas prise en charge.

**Windows Server 2003 et Windows XP :** Définit la taille du cache de fichiers. La taille par défaut du cache est 0x32 (50 Mo).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Cette valeur n’est pas prise en charge.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

Cette valeur n’est pas prise en charge.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Vérifiez ou réparez uniquement les fichiers. Ne vérifiez pas ou ne réparez pas les clés de registre.

**Windows XP :** Non pris en charge.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Utilisez cette option pour les réparations hors connexion. Spécifiez l’emplacement du répertoire de démarrage hors connexion.

**Windows XP :** Non pris en charge.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Utilisez cette option pour les réparations hors connexion. spécifiez l’emplacement du répertoire de Windows hors connexion.

**Windows XP :** Non pris en charge.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Cette valeur n’est pas prise en charge.

**Windows Server 2003 et Windows XP :** Vide le cache de fichiers et analyse tous les fichiers système protégés.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Cette valeur n’est pas prise en charge.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Revenez aux paramètres par défaut.

**Windows Server 2008 et Windows Vista :** Non pris en charge.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>Vérifie
</dt> <dd>

Cette valeur n’est pas prise en charge.

**Windows Server 2003 et Windows XP :** Analyse tous les fichiers système protégés à chaque démarrage.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Analyse et répare le fichier situé dans le chemin d’accès complet spécifié.

**Windows XP :** Non pris en charge.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Analyse immédiatement tous les fichiers système protégés.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Cette valeur n’est pas prise en charge.

**Windows Server 2003 et Windows XP :** Analyse tous les fichiers système protégés au prochain démarrage.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Vérifie le fichier au chemin d’accès complet spécifié. Cette option ne répare pas le fichier.

**Windows XP :** Non pris en charge.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Analyse tous les fichiers système protégés, mais ne répare pas les fichiers.

**Windows XP :** Non pris en charge.

</dd> </dl>

SFC définit la valeur de Registre suivante :

 = HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan

Pour plus d’informations, consultez [valeurs de Registre WFP](wfp-registry-values.md).

## <a name="remarks"></a>Remarques

sur Windows Vista uniquement, vous pouvez définir la variable d’environnement du **\_ \_ journal de suivi Windows** sur l’emplacement d’un répertoire valide pour recevoir un fichier journal.

## <a name="examples"></a>Exemples

Les exemples de lignes de commande suivants sont des exemples de syntaxe de sfc.exe.

**sfc/SCANNOW**

**SFC/VERIFYFILE = c : \\ Windows \\ system32 \\kernel32.dll**

**SFC/SCANFILE = d : \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d : \\ /OFFWINDIR = d : \\ Windows**

**SFC/VERIFYONLY/FILESONLY**

 

 



