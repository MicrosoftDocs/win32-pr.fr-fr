---
description: Le WiPolicy.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple montre comment le script peut être utilisé pour gérer la stratégie système. La stratégie peut être configurée par un administrateur à l’aide de l’éditeur de stratégie de groupe (GPE).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Gérer des paramètres de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86684e75e09fa0a588c2d1d0d999488d6e89fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531801"
---
# <a name="manage-policy-settings"></a>Gérer des paramètres de stratégie

Le WiPolicy.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple montre comment le script peut être utilisé pour gérer la [stratégie système](system-policy.md). La stratégie peut être configurée par un administrateur à l’aide de l’éditeur de stratégie de groupe (GPE).

Cet exemple illustre les stratégies de Windows Installer.

L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiPolicy.vbs \[ valeur de stratégie \] \[\]**

Si aucun argument n’est spécifié sur la ligne de commande, l’exemple retourne les paramètres de stratégie actuels. Spécifiez la stratégie à définir à l’aide des codes d’identificateur suivants. Spécifiez la nouvelle valeur de la stratégie. Pour retourner la valeur actuelle d’une stratégie, spécifiez une chaîne vide «» pour la valeur.



| CODE | Description                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modes de journalisation. Pour plus d’informations, consultez [journalisation](logging.md) .                                                                            |
| DO   | Modes de débogage. Pour plus d’informations, consultez [Debug](debug.md).                                                                                   |
| DI   | Désactivez le mode Windows Installer. Pour plus d’informations, consultez [DisableMsi](disablemsi.md).                                                      |
| WT   | Délai d’attente en secondes en cas d’absence d’activité. **HKLM** \\ **Logiciel** \\ **Stratégies** \\ **Microsoft** \\ **Windows** \\ **Programme d’installation** \\ **Délai d’expiration** |
| DB   | Désactiver l’exploration des emplacements sources par l’utilisateur. Pour plus d’informations, consultez [DisableBrowse](disablebrowse.md).                                     |
| DP   | Désactivez la mise à jour corrective. Pour plus d’informations, consultez [DisablePatch](disablepatch.md).                                                                |
| Unifi   | Propriétés publiques envoyées pour installer le service. Pour plus d’informations, consultez [EnableUserControl](enableusercontrol.md).                             |
| SS   | Programme d’installation sécurisé pour l’écriture de scripts à partir du navigateur. Pour plus d’informations, consultez [SafeForScripting](safeforscripting.md).                               |
| EM   | Privilèges système (HKLM). Pour plus d’informations, consultez [AlwaysInstallElevated a](alwaysinstallelevated.md).                                      |
| EU   | Privilèges système (HKCU). Pour plus d’informations, consultez [AlwaysInstallElevated a](alwaysinstallelevated.md).                                      |
| DR   | Désactivez la stratégie de restauration. Pour plus d’informations, consultez [DisableRollback](disablerollback.md).                                                   |
| TS   | Localisez les transformations à la racine de l’image source. Pour plus d’informations, consultez [stratégie TransformsAtSource](transformsatsource-policy.md).             |
| TP   | Épingler les transforme sécurisés dans le cache côté client. Pour plus d’informations, consultez [stratégie TransformsSecure](transformssecure-policy.md).                 |
| SO   | Ordre de recherche des types de sources. Pour plus d’informations, consultez [SearchOrder](searchorder.md).                                                      |



 

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



