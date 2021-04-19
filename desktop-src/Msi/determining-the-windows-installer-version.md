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
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="5e065-103">Détermination de la version de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5e065-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="5e065-104">Vous pouvez utiliser les méthodes suivantes pour déterminer la version de Windows Installer :</span><span class="sxs-lookup"><span data-stu-id="5e065-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="5e065-105">Appelez la fonction [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) avec le paramètre *szFilePath* défini sur le chemin d’accès au fichier Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="5e065-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="5e065-106">Vous pouvez appeler la fonction [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) avec la **constante \_ système CSIDL** pour récupérer le chemin d’accès à Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="5e065-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="5e065-107">À compter de Windows Vista, les applications doivent utiliser la fonction [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) et le système **REFKNOWNFOLDERID** .</span><span class="sxs-lookup"><span data-stu-id="5e065-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="5e065-108">Les applications existantes qui utilisent la fonction **SHGetFolderPath** et le type **CSIDL** continuent de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="5e065-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="5e065-109">La valeur de la propriété [**installer. version**](installer-version.md) de l' [**objet installer**](installer-object.md) est équivalente aux chaînes à quatre champs figurant dans les [versions commercialisées de Windows Installer](released-versions-of-windows-installer.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="5e065-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="5e065-110">Les applications peuvent récupérer la version Windows Installer à l’aide de [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="5e065-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="5e065-111">Le programme d’installation définit la propriété [**VersionMsi**](versionmsi.md) sur la version de Windows Installer qui est exécutée pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="5e065-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="5e065-112">Pour plus d’informations, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="5e065-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
