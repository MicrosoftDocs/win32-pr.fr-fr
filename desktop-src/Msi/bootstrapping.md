---
description: Actuellement, chaque installation qui tente d’utiliser le Windows Installer commence par vérifier si le programme d’installation est présent sur l’ordinateur de l’utilisateur et, s’il n’est pas présent, si l’utilisateur et l’ordinateur sont prêts à installer Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Amorçage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527434"
---
# <a name="bootstrapping"></a>Amorçage

Actuellement, chaque installation qui tente d’utiliser le Windows Installer commence par vérifier si le programme d’installation est présent sur l’ordinateur de l’utilisateur et, s’il n’est pas présent, si l’utilisateur et l’ordinateur sont prêts à installer Windows Installer. Une application d’installation [Instmsi.exe](instmsi-exe.md) est disponible avec le kit de développement logiciel (SDK) Windows Installer qui contient la logique et les fonctionnalités d’installation de Windows Installer. Toutefois, une application d’amorçage doit gérer cette installation.

L’application d’amorçage doit tout d’abord vérifier si Windows Installer est actuellement installé. Les applications peuvent récupérer la version de Windows Installer actuellement installée à l’aide de [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Si Windows Installer n’est pas installé actuellement, l’application d’amorçage doit interroger le système d’exploitation pour déterminer quelle version du Instmsi.exe est requise. Une fois que l’installation de Windows Installer a démarré, l’application d’amorçage doit gérer les codes de retour de l’application Instmsi.exe et gérer tout redémarrage qui survient au cours de l’installation de Windows Installer. Pour plus d’informations, consultez [détermination de la version de Windows Installer](determining-the-windows-installer-version.md)

L’exemple suivant montre comment l’application d’installation qui installe Microsoft Office 2000 vérifie le système de l’utilisateur et configure l’installation Windows Installer. Cet exemple est écrit spécifiquement pour installer Office 2000 et doit être utilisé comme référence générale uniquement.

Quand un utilisateur insère un CD-ROM Office 2000 sur son ordinateur, Setup.exe tente de lancer le mode de maintenance, l’application d’installation ou rien du tout en fonction des besoins de l’utilisateur. La section suivante décrit comment l’application d’installation Office 2000, nommée Setup.exe, qualifie l’utilisateur et son ordinateur, crée une ligne de commande et installe Windows Installer à l’aide de l’application Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Comment Setup.exe amorce le Windows Installer lors de l’installation d’Office 2000

1.  L’utilisateur insère un CD-ROM Office 2000 sur son ordinateur. Le système d’exploitation Windows lance Setup.exe à l’aide du commutateur/autorun et du fichier autorun. inf. Le fichier autorun. inf se trouve à la racine du CD-ROM Office 2000 et contient les sections suivantes :

    \[Autorun\]

     

    \[Fonctionnalités Office\]

     

    \[Informations sur le produit\]

     

    \[ServicePack \] .

    La \[ \] section autorun contient une ligne de commande qui exécute l’application Setup.exe, exécute l’icône utilisée pour afficher le disque et contient des informations pour ajouter une option « installer » et une option « configurer » au menu contextuel du CD-ROM.

    La \[ section fonctionnalités Office \] contient une liste de fonctionnalités et de paires de noms de fonctionnalités.

    La \[ section informations sur le produit \] spécifie le nom et la version de l’application.

    La \[ \] section ServicePack permet à un administrateur réseau de définir le niveau de Service Pack minimal requis. L’administrateur réseau peut utiliser cette section pour créer le texte d’un message d’alerte affiché si le système d’exploitation local ne dispose pas de l’Service Pack requis.

    Voici un exemple de fichier autorun. inf.

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  L’application Setup.exe recherche le \_ mutex MsiPromptForCD. Windows Installer crée ce mutex lorsqu’il invite l’utilisateur à insérer le CD-ROM. La présence du mutex indique que Windows Installer exécute une installation qui a demandé le CD-ROM Office 2000. Dans ce cas, l’application Setup.exe s’arrête immédiatement et permet à l’installation d’Office 2000 de continuer. Si le mutex est absent, l’application Setup.exe continue à l’étape 3 où une clé de Registre est évaluée pour déterminer si Office 2000 est installé.
3.  L’application Setup.exe vérifie la présence de la clé de Registre Office9 :

    **HKCU/Software/Microsoft/Office/9.0/common/General/InstallProductID**

    Si cette clé de Registre n’existe pas, l’application Setup.exe continue à l’étape 6 où le système d’exploitation est vérifié pour déterminer si elle est qualifiée pour l’installation d’Office 2000.

4.  Si la clé de Registre Office 2000 existe, l’application Setup.exe vérifie l’état d’installation actuel en appelant [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Un état de retour de InstallState \_ default indique qu’Office 2000 est déjà installé et que l’application Setup.exe se poursuit à l’étape 5, où l’exécution de la source office 2000 est vérifiée.

    Si Office 2000 n’est pas installé, l’application Setup.exe continue à l’étape 6 où le système d’exploitation est vérifié pour déterminer si elle est qualifiée pour l’installation d’Office 2000.

5.  L’application Setup.exe appelle [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) pour chacune des fonctionnalités de la section **\[ OfficeFeatures \]** du fichier autorun. inf. Si l’une de ces fonctionnalités retourne \_ la source INSTALLSTATE, cela indique que la fonctionnalité est exécutée à partir de la source et que l’application Setup.exe s’arrête immédiatement.

    Si aucune des fonctionnalités ne retourne \_ la source INSTALLSTATE, l’application Setup.exe lance l’application du programme d’installation, Msiexec.exe et présente le mode de maintenance Windows Installer avant de quitter.

6.  L’application Setup.exe détermine si le système d’exploitation est qualifié pour une installation d’Office 2000. Windows XP est requis pour installer Office 2000. Si le système d’exploitation requiert une mise à jour Service Pack pour être éligible à Office 2000, l’application Setup.exe affiche le texte spécifié dans le fichier autorun. inf. Si le système d’exploitation n’est pas éligible à Office 2000 ou à une mise à niveau d’Office 2000, l’application Setup.exe affiche un message qui empêche l’utilisateur de continuer.

    Si le système d’exploitation qualifie Office 2000, l’application Setup.exe continue à l’étape 7, qui détermine si Windows Installer est installé sur l’ordinateur de l’utilisateur.

7.  Si Windows Installer existe sur l’ordinateur de l’utilisateur, l’application Setup.exe lance l’application Msiexec.exe et lui transmet le fichier Office 2000. msi.

    Si Windows Installer n’est pas installé sur l’ordinateur local, l’application Setup.exe se poursuit à l’étape 8, qui détermine si le système d’exploitation est qualifié pour l’installation de Windows Installer.

8.  Si l’ordinateur local est autorisé à avoir Windows Installer installé, l’application Setup.exe exécute la version appropriée de l’application Instmsi.exe installer pour la plateforme. Setup.exe pouvez passer le commutateur de ligne de commande « /q » pour supprimer l’interface utilisateur et empêcher l’utilisateur de modifier les options de configuration de l’installation.
9.  L’application Setup.exe charge le fichier Msi.dll récemment installé et effectue un appel à la fonction [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) pour installer l’application de l’utilisateur.

## <a name="setupexe-command-line-parameters"></a>Setup.exe les paramètres de ligne de commande

L’application Setup.exe permet aux administrateurs et aux utilisateurs de passer des options de ligne de commande à l’application Msiexec.exe. Pour plus d’informations, consultez [options de ligne de commande](command-line-options.md). Le tableau suivant répertorie les options de commande qui peuvent être utilisées avec Setup.exe.



| Option                       | Usage                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe/autorun                                                                                                                           | Exécute le fichier autorun. inf décrit ci-dessus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Lance une installation administrative.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[\| \] *package* u m ou <br/> \[\|liste des \] *transformations* du *package* u m<br/> ou <br/> \[\|package u m m \]  /g *LanguageID*<br/> | Publie un produit. Cette option ignore toutes les valeurs de propriété entrées sur la ligne de commande. Publier sur l’utilisateur actuel.<br/> Publier sur tous les utilisateurs de l’ordinateur.<br/> identificateur de langue g<br/> t applique la transformation au package publié.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t ProgramMgmt. MST                                                                                                  | Spécifie le fichier. msi que Setup.exe doit installer. Si l’option/I n’est pas incluse, Setup.exe utilise le fichier Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o< = *valeur* de la propriété> | setup.exe/o CDKEY = 111111-1111                                                                                                               | Définit les propriétés dans le fichier. msi. Setup.exe le transmet à msiexec comme écrit.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | Définissez le niveau d’interface utilisateur de l’installation. /q aucune interface utilisateur (/qn pour MsiExec.)/QB interface utilisateur de base<br/> /QR interface utilisateur réduite.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe/M4                                                                                                                                | Prend en charge plusieurs licences conformément aux contrats sélectionnés. Cette propriété est utilisée par l’action personnalisée de vérification de licence pour écrire le certificat LV. L’option/m doit être suivie du nombre de déverrouillages autorisés. La valeur spécifiée par l’option/m doit être définie en tant que propriété « M » dans le fichier Office9.msi. Si aucune valeur n’est spécifiée, mais que l’option/m est utilisée avec le programme d’installation, la valeur 0 doit être définie. L’option/m est requise pour prendre en charge les clients Select à l’aide d’un CD ou d’un réseau. |
| /Settings                    | setup.exe/Settings mysettings.ini                                                                                                           | Permet aux administrateurs de spécifier un fichier. ini contenant tous les paramètres personnalisés à passer lors de l’installation d’Office 2000. Consultez la description du fichier. ini ci-dessous.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Utilisation d’un fichier. ini

La création d’un fichier d’initialisation peut être plus facile que la création d’une ligne de commande longue. À l’aide de l’option/Settings, l’application Setup.exe lit le fichier. ini spécifié et construit une ligne de commande à passer à l’application Msiexec.exe. Seules les propriétés prises en charge sur la ligne de commande sont prises en charge dans le fichier. ini. Si une propriété ou une valeur se trouve à la fois dans le fichier. ini et sur la ligne de commande, les paramètres de ligne de commande remplacent les paramètres du fichier. ini.

Le format du fichier. ini est le suivant :

\[msi\]

 

\[débit maximal acceptable\]

 

\[options\]

 

\[Afficher\]

La \[ \] section MSI du fichier. ini spécifie le chemin d’accès au package d’installation pour l’installation. Cela correspond à l’option/I sur la ligne de commande.

La \[ \] section MST du fichier. ini spécifie le chemin d’accès aux transformations utilisées avec cette installation. Cela correspond à l’option/j sur la ligne de commande. Plusieurs transformations sont indiquées sur une autre ligne, à l’aide de MST1 MST (N). Lorsqu’elle est analysée dans la ligne de commande, la liste dans le fichier. ini est retournée de gauche à droite. Notez que le nombre associé au titre MST (N) est présent uniquement pour gérer des identificateurs uniques et n’a aucune signification par programmation.

La \[ \] section Options permet aux administrateurs réseau de définir et de remplacer des propriétés dans les fichiers. msi ou. MST. Les options définies dans le fichier. ini sont ajoutées à la ligne de commande à l’aide de l’option/o. Chaque option de la section option doit avoir un nom de propriété et une valeur.

La \[ section Affichage permet \] de définir le niveau d’interface utilisateur utilisé lors de l’installation. Cela correspond à l’option/q sur la ligne de commande. Les valeurs valides sont None, Basic, Reduced et Full.

Exemple de fichier. ini

\[MSI\]

 

MSI = \\ \\ sourceshare \\ office2000 \\Office2000.msi

 

\[DÉBIT maximal acceptable\]

 

MST1 = \\ \\ sourceshare \\ office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ office2000 \\ trns2. MST

 

\[Options\]

 

PUBLICPROPERTY = votre valeur

\[Afficher\]

 

Affichage = aucun

 

