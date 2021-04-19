---
description: 'Vous pouvez utiliser les méthodes suivantes pour déterminer la version de Windows Installer :'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Détermination de la version de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528206"
---
# <a name="determining-the-windows-installer-version"></a>Détermination de la version de Windows Installer

Vous pouvez utiliser les méthodes suivantes pour déterminer la version de Windows Installer :

-   Appelez la fonction [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) avec le paramètre *szFilePath* défini sur le chemin d’accès au fichier Msi.dll.

    Vous pouvez appeler la fonction [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) avec la **constante \_ système CSIDL** pour récupérer le chemin d’accès à Msi.dll. À compter de Windows Vista, les applications doivent utiliser la fonction [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) et le système **REFKNOWNFOLDERID** . Les applications existantes qui utilisent la fonction **SHGetFolderPath** et le type **CSIDL** continuent de fonctionner.

-   La valeur de la propriété [**installer. version**](installer-version.md) de l' [**objet installer**](installer-object.md) est équivalente aux chaînes à quatre champs figurant dans les [versions commercialisées de Windows Installer](released-versions-of-windows-installer.md) rubrique.
-   Les applications peuvent récupérer la version Windows Installer à l’aide de [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   Le programme d’installation définit la propriété [**VersionMsi**](versionmsi.md) sur la version de Windows Installer qui est exécutée pendant l’installation.

Pour plus d’informations, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

 

 
