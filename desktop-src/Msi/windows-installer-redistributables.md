---
description: le Windows Installer redistribuable est un package de mises à jour logicielles.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Redistribuables Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 9fc175a96ae1d2daed9798981b0dbe679505975e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416864"
---
# <a name="windows-installer-redistributables"></a>Redistribuables Windows Installer

Windows Le programme d’installation 4,5 et versions antérieures est disponible en tant que package de mise à jour logicielle redistribuable. consultez la section [versions publiées de Windows Installer](released-versions-of-windows-installer.md) pour déterminer les produits livrés avec les versions de Windows Installer. le package de mise à jour redistribuable pour une version est mis à disposition après la publication du produit livré avec une version de Windows Installer spécifique.

> [!NOTE]
> il n’existe aucun redistribuable pour Windows Installer 5,0. cette version est incluse avec le système d’exploitation dans Windows 7, Windows server 2008 R2, et versions ultérieures du client et du serveur (y compris Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>obtention de la Windows Installer redistribuable (4,5 et versions antérieures)

-   vous pouvez trouver tous les redistribuables Windows Installer disponibles dans le [centre de téléchargement Microsoft](https://www.microsoft.com/Downloads/).
-   le téléchargement pour le [package redistribuable Windows Installer 4,5](https://support.microsoft.com/kb/942288) est disponible à l’adresse suivante : https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs x86 exécutant Windows vista, Windows vista avec Service Pack 1 (SP1) et Windows Server 2008 est Windows 6.0-kb942288-v2-x86. MSU.
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs x64 exécutant Windows vista, Windows vista avec SP1 et Windows Server 2008 est Windows 6.0-kb942288-v2-x64. MSU.
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs Itanium-Based Systems exécutant Windows vista, Windows vista avec SP1 et Windows Server 2008 est Windows 6.0-kb942288-v2-ia64. MSU.
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs x86 exécutant Windows xp avec service pack 2 (SP2) et Windows xp avec service pack 3 (SP3) est WindowsXP-KB942288-v3-x86.exe.
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs x86 exécutant Windows server 2003 avec service pack 1 (SP1) et Windows server 2003 avec service pack 2 (SP2) est WindowsServer2003-KB942288-v4-x86.exe.
-   le nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs x64 exécutant Windows server 2003 avec SP1 et Windows server 2003 avec SP2 est WindowsServer2003-KB942288-v4-x64.exe.
-   nom du package redistribuable qui installe Windows Installer 4,5 sur les ordinateurs Itanium-Based Systems exécutant Windows server 2003 avec SP1 et Windows server 2003 avec SP2 est WindowsServer2003-KB942288-v4-ia64.exe.
-   il n’existe aucun redistribuable qui installe Windows Installer 4,0. cette version du Windows Installer est fournie avec Windows Vista.
-   le nom du redistribuable qui installe Windows Installer 3,1 est WindowsInstaller-KB893803-v2-x86.exe. le téléchargement du package [Windows Installer 3,1 redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) est disponible à l’adresse suivante : https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > si vous avez effectué une mise à niveau vers Windows Installer 3,1 en installant Windows server 2003 avec SP1, ou une version antérieure de ce package redistribuable, vous devrez peut-être également installer la [mise à jour pour Windows server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) pour obtenir toutes les mises à jour disponibles dans [Windows Installer redistributable 3,1 (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c).

     

-   le redistribuable qui installe Windows Installer 3,0 est WindowsInstaller-KB884016-v2-x86.exe. le téléchargement de la [Windows Installer 3,0 redistribuable](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) est disponible à l’adresse suivante : https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   le Windows Installer 2,0 a utilisé une convention d’affectation de noms précédente pour le package redistribuable : [Instmsi.exe](instmsi-exe.md). le package redistribuable pour l’installation ou la mise à niveau vers Windows Installer 2,0 sur Windows 2000 ne doit pas être utilisé pour installer ou mettre à niveau Windows Installer 2,0 sur Windows Server 2003 et Windows XP.

    le téléchargement de la [Windows Installer 2,0 redistributable pour Windows NT 4,0 et Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) est disponible à l’adresse https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>installation du Windows Installer redistribuable (4,5 et versions antérieures)

le Windows Installer 4,5 resdistributable est fourni pour les systèmes d’exploitation Windows Vista et Windows Server 2008 sous la forme d’un fichier. msu et doit être installé à l’aide du [programme d’installation Windows Update autonome](https://support.microsoft.com/kb/934307/) (Wusa.exe.)

le Windows Installer redistribuable 4,5 pour les systèmes d’exploitation Windows XP et Windows Server 2003 peut être installé à l’aide de la syntaxe et des options de ligne de commande suivantes.

les fichiers redistribuables Windows Installer 3,1 et Windows Installer 3,0 peuvent être installés à l’aide de la syntaxe de ligne de commande et des options suivantes.

### <a name="syntax"></a>Syntaxe

utilisez la syntaxe suivante pour installer les fichiers redistribuables pour Windows Installer 4,5 sur Windows XP et Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Options de ligne de commande

les packages de mises à jour logicielles redistribuables Windows Installer utilisent les options de ligne de commande qui ne respectent pas la casse.



| Option     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Empêche le package redistribuable de demander à l’utilisateur de redémarrer, même s’il devait remplacer des fichiers qui étaient en cours d’utilisation pendant l’installation. Si le package de mise à jour est appelé avec cette option, il retourne l' **erreur \_ échec du \_ redémarrage \_ requis** s’il devait remplacer les fichiers qui étaient en cours d’utilisation.<br/> S’il n’a pas été nécessaire de remplacer les fichiers qui étaient en cours d’utilisation, il renvoie une **erreur \_**. Pour plus d’informations sur les redémarrages différés, consultez la section Notes.<br/> |
| /quiet     | pour une utilisation par les applications qui redistribuent les Windows Installer dans le cadre d’une application d’amorçage. Une interface utilisateur n’est pas présentée à l’utilisateur. l’application d’amorçage doit vérifier le code de retour pour déterminer si un redémarrage est nécessaire pour terminer l’installation du Windows Installer.<br/>                                                                                                                                                |
| /help      | Affiche de l’aide sur toutes les options disponibles.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>redémarrage différé sur Windows Vista et Windows Server 2008

L’option de ligne de commande/norestart empêche wusa.exe de redémarrer l’ordinateur. Toutefois, si un fichier mis à jour par le package MSU est en cours d’utilisation, le package n’est pas appliqué à l’ordinateur jusqu’à ce que l’utilisateur redémarre l’ordinateur. cela signifie que les applications qui utilisent le redistribuable Windows Installer 4,5 pour Windows Vista et Windows Server 2008 ne peuvent pas utiliser la fonctionnalité Windows Installer 4,5 tant que l’ordinateur n’a pas redémarré.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>redémarrage différé sur Windows XP et Windows Server 2003

il est recommandé d’arrêter le service Windows Installer lors de l’utilisation du package de mise à jour. lorsque le package est exécuté en mode d’interface utilisateur complet, il détecte si le service Windows Installer est en cours d’exécution et demande à l’utilisateur d’arrêter le service. si l’utilisateur continue sans arrêter le service, la mise à jour remplace Windows Installer.

les applications d' [amorçage](bootstrapping.md) qui utilisent le package redistribuable pour installer le Windows Installer avec une autre application peuvent nécessiter un redémarrage du système supplémentaire en plus des redémarrages nécessaires pour installer l’application. L’option redémarrage différé est recommandée dans les cas où il est nécessaire d’éliminer un redémarrage supplémentaire provoqué par l’installation de fichiers en cours d’utilisation. Les développeurs doivent effectuer les opérations suivantes dans leur application d’installation pour utiliser l’option redémarrage différé.

-   Appelez le package redistribuable avec l’option de ligne de commande/norestart.
-   Traitez le retour du **\_ succès** de l’erreur ou de la réussite de l' **erreur \_ \_ \_** .
-   Appelez msiexec sur le package de l’application et exécutez un autre code d’installation spécifique à l’application. Si l’application d’installation utilise [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), l’application doit charger MSI.DLL à partir du répertoire système. si aucun redémarrage n’a lieu et si le redistribuable a retourné une **erreur de \_ \_ redémarrage \_ requis**, puis invite l’utilisateur à redémarrer pour terminer l’installation des fichiers binaires du Windows Installer. Si un redémarrage se produit, aucune étape supplémentaire n’est requise.
    > [!Note]  
    > Les applications qui appellent [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sur le nouveau MSI.DLL une fois que le package redistribuable retourne une réussite doivent s’assurer qu’une version antérieure de MSI.DLL n’a pas déjà été chargée dans le processus. Si une version antérieure de MSI.DLL a été chargée, elle doit être déchargée de l’espace d’adressage du processus avant d’appeler **LoadLibrary** pour la nouvelle MSI.DLL.

     

pour plus d’informations, consultez [Windows Installer l’amorçage](windows-installer-bootstrapping.md).

 

 
