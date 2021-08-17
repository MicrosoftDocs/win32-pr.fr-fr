---
description: Instmsi.exe est le package redistribuable pour l’installation de Windows Installer&\# 160 ; 2.0 et des versions antérieures de Windows Installer. consultez Windows Installer redistribuables pour les redistribuables pour Windows Installer&\# 160 ; 3.0 et versions ultérieures.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946117"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe est le package redistribuable pour l’installation de Windows Installer 2,0 et des versions antérieures de Windows Installer. consultez [Windows Installer redistribuables](windows-installer-redistributables.md) pour les redistribuables pour Windows Installer 3,0 et versions ultérieures.

pour plus d’informations sur la version de la Windows Installer qui a été fournie avec votre système d’exploitation, consultez [Versions publiées de Windows Installer](released-versions-of-windows-installer.md).

Certains redistribuables ne doivent pas être exécutés sur certaines versions du système d’exploitation. Le tableau suivant décrit le Instmsi est compatible avec le système d’exploitation.



| si Instmsi.exe installe cette version du Windows Installer | Instmsi.exe peuvent être exécutés sur ces systèmes d’exploitation                    | Instmsi.exe ne doit pas être exécuté sur ces systèmes d’exploitation                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Programme d’installation 1,0                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows Me, Windows 2000, Windows XP, Windows server 2003, Windows Vista, Windows server 2008 |
| Windows Programme d’installation 1,1                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows Me, Windows 2000, Windows XP, Windows server 2003, Windows Vista, Windows server 2008 |
| Windows Programme d’installation 1,2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0 + SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Programme d’installation 2,0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0 + SP6, Windows 2000 | Windows XP, Windows server 2003, Windows Vista, Windows server 2008                           |



 

par exemple, une application qui redistribue Windows Installer version 1,1 doit vérifier que le système d’exploitation est Windows NT 4,0 SP3 ou Windows 98/95 avant d’exécuter le package redistribuable. les Applications qui utilisent le package redistribuable doivent également s’assurer que la version ANSI du Windows Installer est installée sur Windows 98/95 et que la version Unicode est installée sur Windows NT ou Windows 2000. Notez que certaines applications renomment la version Unicode en InstMsiW.

## <a name="syntax"></a>Syntaxe

 *options* Instmsi

## <a name="command-line-options"></a>Options de la ligne de commande

Les options de ligne de commande ne respectent pas la casse.



| Option                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | pour une utilisation par les applications qui redistribuent les Windows Installer dans le cadre d’une application d’amorçage. Aucune interface utilisateur n’est présentée à l’utilisateur. l’application d’amorçage doit vérifier le code de retour pour déterminer si un redémarrage est nécessaire pour terminer l’installation du Windows Installer.                                                                                                                                                                                                                          |
| /t                         | Utilisé à des fins de débogage uniquement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c : "msiinst/delayreboot"  | Option redémarrage différé. Empêche Instmsi de demander à l’utilisateur un redémarrage même s’il devait remplacer des fichiers qui étaient en cours d’utilisation pendant l’installation. Si Instmsi est appelé avec cette option, il retourne une erreur \_ de \_ redémarrage de la réussite \_ obligatoire s’il a dû remplacer des fichiers qui étaient en cours d’utilisation. S’il n’a pas été nécessaire de remplacer les fichiers qui étaient en cours d’utilisation, il renvoie une erreur \_ . disponible avec Instmsi pour Windows Installer 2,0 ou version ultérieure. Pour plus d’informations sur les redémarrages différés, consultez la section Notes.<br/> |
| /c : "msiinst/delayrebootq" | Version en mode silencieux de l’option redémarrage différé. Elle ne présente pas d’interface utilisateur à l’utilisateur. Dans le cas contraire, le comportement est identique à l’option précédente. disponible avec Instmsi pour Windows Installer 2,0 ou version ultérieure. Pour plus d’informations sur les redémarrages différés, consultez la section Notes.<br/>                                                                                                                                                                                                                           |
| /?                         | Affiche de l’aide.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Remarques

les applications d' [amorçage](bootstrapping.md) qui utilisent Instmsi.exe pour installer le Windows Installer avec une autre application peuvent nécessiter un redémarrage du système supplémentaire. Il peut s’agit d’un redémarrage supplémentaire en plus des redémarrages nécessaires pour installer l’application.

L’option redémarrage différé est recommandée pour les développeurs de programme d’installation qui souhaitent éliminer un redémarrage supplémentaire provoqué par l’utilisation de Instmsi.exe avec une application d’installation qui installe les fichiers en cours d’utilisation.

Les développeurs doivent effectuer les opérations suivantes dans leur application d’installation pour utiliser l’option redémarrage différé. Cette option n’est pas disponible avec les versions Instmsi.exe qui installent les versions de Windows Installer antérieures à la version 2,0 :

**Pour utiliser l’option redémarrage différé**

1.  Appelez Instmsi.exe avec l’une des options de ligne de commande reboot retardée.
2.  Traitez le retour du succès de l’erreur ou de la réussite de l' \_ erreur \_ \_ \_ .
3.  récupérez le chemin d’accès au dossier contenant les binaires de Windows Installer récemment installés à partir de la valeur InstallerLocation sous :

    **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer**

    Cette valeur est de type **reg \_ SZ**.

4.  Définissez le répertoire actif sur le chemin d’accès obtenu à l’étape 3.
5.  Appelez msiexec sur le package de l’application et exécutez un autre code d’installation spécifique à l’application. Si l’application d’installation utilise [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), l’application doit charger MSI.DLL à partir de l’emplacement obtenu à l’étape 3.
    > [!Note]  
    > Les applications qui appellent **LoadLibrary** sur le nouvel MSI.DLL à l’emplacement obtenu à l’étape 3 doivent s’assurer qu’une version antérieure de MSI.DLL n’a pas déjà été chargée dans le processus. Si une version antérieure de MSI.DLL a été chargée dans le processus, elle doit être déchargée de l’espace d’adressage du processus avant l’appel de **LoadLibrary** pour la nouvelle MSI.DLL.

     

6.  si l’étape (5) ne nécessite pas de redémarrage et si Instmsi.exe a retourné une erreur de redémarrage de la \_ réussite \_ \_ requise à l’étape (1), invitez l’utilisateur à redémarrer pour terminer l’installation des fichiers binaires Windows Installer sur le système. Toutefois, si un redémarrage se produit à l’étape (5), aucune étape supplémentaire n’est requise.

Instmsi.exe est disponible dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amorçage](bootstrapping.md)
</dt> <dt>

[Amorçage du téléchargement Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> </dl>

 

 




