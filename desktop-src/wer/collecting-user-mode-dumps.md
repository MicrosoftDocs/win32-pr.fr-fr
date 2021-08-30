---
title: Collecte des vidages de User-Mode
description: à compter de Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1), Rapport d’erreurs Windows (WER) peut être configuré de sorte que les vidages en mode utilisateur complets soient collectés et stockés localement après une panne d’application en mode utilisateur.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890dfbe297e5448d831ce2f149777a66db5ef7e7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473055"
---
# <a name="collecting-user-mode-dumps"></a>Collecte des vidages de User-Mode

à compter de Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1), Rapport d’erreurs Windows (WER) peut être configuré de sorte que les vidages en mode utilisateur complets soient collectés et stockés localement après une panne d’application en mode utilisateur. Les applications qui effectuent leurs propres rapports d’incident personnalisés, y compris les applications .NET, ne sont pas prises en charge par cette fonctionnalité.

Cette fonctionnalité n’est pas activée par défaut. L’activation de la fonctionnalité requiert des privilèges d’administrateur. pour activer et configurer la fonctionnalité, utilisez les valeurs de registre suivantes sous la clé **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ Rapport d’erreurs Windows \\ LocalDumps** .


| Valeur | Description | Type | Valeur par défaut | 
|-------|-------------|------|---------------|
| <strong>DumpFolder</strong> | Chemin d’accès où les fichiers de vidage doivent être stockés. Si vous n’utilisez pas le chemin d’accès par défaut, assurez-vous que le dossier contient des listes de contrôle d’accès qui permettent au processus de blocage d’écrire des données dans le dossier. Pour les pannes de service, le vidage est écrit dans des dossiers de profil spécifiques au service en fonction du compte de service utilisé. Par exemple, le dossier de profil des services système est%WINDIR%\System32\Config\SystemProfile. Pour les services réseau et locaux, le dossier est%WINDIR%\ServiceProfiles.<br /> | REG_EXPAND_SZ | %LOCALAPPDATA%\CrashDumps | 
| <strong>DumpCount</strong> | Nombre maximal de fichiers de vidage dans le dossier. Lorsque la valeur maximale est dépassée, le fichier de vidage le plus ancien dans le dossier sera remplacé par le nouveau fichier de vidage. | REG_DWORD | 10 | 
| <strong>DumpType</strong> | Spécifiez l’un des types de vidages suivants :<ul><li>0 : vidage personnalisé</li><li>1 : mini-vidage</li><li>2 : vidage complet</li></ul> | REG_DWORD | 1 | 
| <strong>CustomDumpFlags</strong> | Options de vidage personnalisées à utiliser. Cette valeur est utilisée uniquement lorsque <strong>DumpType</strong> a la valeur 0.<br /> Les options sont une combinaison au niveau du bit des valeurs d’énumération <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .<br /> | REG_DWORD | <code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData = = 0x00000001 | 0x00000020 | 0x00000100</code> | 


>[!NOTE]
> Un vidage sur incident n’est pas collecté lorsque vous définissez le [débogage automatique pour les blocages d' **application**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes). 

Ces valeurs de Registre représentent les paramètres globaux. Vous pouvez également fournir des paramètres par application qui remplacent les paramètres globaux. pour créer un paramètre par application, créez une clé pour votre application sous **HKEY \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Rapport d’erreurs Windows \\ LocalDumps** (par exemple, **hkey \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Rapport d’erreurs Windows \\ LocalDumps \\MyApplication.exe**). Ajoutez vos paramètres de vidage sous la clé **MyApplication.exe** . Si votre application se bloque, le WER commence par lire les paramètres globaux, puis remplace l’un des paramètres par vos paramètres spécifiques à votre application.

Quand une application se bloque et avant son arrêt, le système vérifie les paramètres du Registre pour déterminer si un vidage local doit être collecté. Une fois la collecte de vidage terminée, l’application est autorisée à se terminer normalement. Si l’application prend en charge la récupération, le vidage local est collecté avant l’appel du rappel de récupération.

Ces vidages sont configurés et contrôlés indépendamment du reste de l’infrastructure WER. Vous pouvez utiliser la collection de vidages locaux même si le rapport d’erreurs Windows est désactivé ou si l’utilisateur annule la création de rapports WER. Le vidage local peut être différent de celui envoyé à Microsoft.

 

