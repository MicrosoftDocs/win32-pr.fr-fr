---
title: empaquetage, déploiement et interrogation d’applications Windows
description: créer par programme des packages d’application pour les applications Windows, et installer, mettre à jour, interroger et désinstaller des packages d’application.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814272"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>empaquetage, déploiement et interrogation d’applications Windows

vous déployez, gérez et service Windows applications (y compris les applications UWPs et de bureau) par le biais de packages d’application. msix/. appx basés sur le format OPC. Chaque package d’application contient les fichiers qui constituent l’application, ainsi qu’un fichier manifeste qui décrit le logiciel à Windows.

## <a name="introduction"></a>Introduction

En règle générale, les développeurs créent et signent des packages d’application à l’aide de Visual Studio. Pour plus d’informations, consultez [empaqueter une application UWP avec Visual Studio](/windows/msix/package/packaging-uwp-apps).

le Microsoft Store facilite la création, l’envoi et la vente de vos applications à des clients dans le monde entier. Pour plus d’informations, consultez [envois d’applications](/windows/uwp/publish/app-submissions).

les applets de commande Windows PowerShell vous permettent d’installer et de gérer des applications métier Windows sans utiliser le Store. Pour plus d’informations, consultez applets de commande du [module AppX](/powershell/module/appx/index?view=win10-ps).

À l’aide des API de Packaging, de déploiement et de requête, vous pouvez effectuer ces tâches par programme :

-   créer un package d’application pour une application Windows
-   déployer une application Windows empaquetée
-   Énumérer les packages d’application installés sur un système et obtenir des informations à leur sujet à partir de leur manifeste
-   Utiliser le contenu d’un package d’application

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                    | Description                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Guide pratique pour créer un package d’application (C++)](how-to-create-a-package.md)                                        | Découvrez comment créer un package d’application à l’aide de l’API de Packaging.                                                                                                                           |
| [Création d’un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md)      | Découvrez comment utiliser [**Makecert**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) pour créer un certificat de signature de code de test afin de pouvoir signer vos packages d’application. |
| [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md)                    | Découvrez comment utiliser [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer vos packages d’application afin qu’ils puissent être déployés.                                                                    |
| [Comment résoudre les erreurs de signature de package d’application](how-to-troubleshoot-app-package-signature-errors.md) | L’échec d’un déploiement d’application peut être dû à l’impossibilité de valider la signature numérique du package d’application. Découvrez comment reconnaître ces échecs et comment les utiliser.          |
| [Comment signer par programmation un package d’application (C++)](how-to-programmatically-sign-a-package.md)          | Découvrez comment signer un package d’application à l’aide de la fonction [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .                                                                                   |
| [Comment développer une application OEM qui utilise un fichier personnalisé](how-to-develop-oem-app-with-custom-file.md)         | Découvrez comment développer une application qui utilise un fichier personnalisé pour transmettre des informations de l’OEM à l’application.                                                                                             |
| [Extraire le contenu du package d’application (C++)](how-to-extract-content-from-a-package.md)                          | Découvrez comment extraire des fichiers d’un package d’application à l’aide de l’API de Packaging.                                                                                                               |
| [Informations sur le manifeste du package d’application de requête (C++)](how-to-query-package-identity-information.md)                   | Découvrez comment obtenir des informations à partir d’un manifeste de package d’application à l’aide de l’API de Packaging                                                                                                            |
| [Dépannage](troubleshooting.md)                                                                   | Fournit des informations pour vous aider à résoudre les problèmes que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application.                                                                 |
| [Référence de l’API de Packaging](interfaces.md)                                                                | L’API de Packaging crée, lit et écrit des packages d’application.                                                                                                                            |
| [Informations de référence sur l’API de déploiement](package-deployment-api.md)                                                   | L’API de déploiement installe, met à jour et désinstalle des packages d’application.                                                                                                                    |
| [Référence API de requête](functions.md)                                                                     | L’API de requête obtient des informations sur les packages d’application installés sur le système.                                                                                                               |
| [Outils et applets de commande PowerShell](appx-packaging-tools.md)                                                 | Utilisez ces outils et applets de commande pour créer, installer et gérer des packages d’application.                                                                                                              |
| [Exemples de Kits de développement logiciel (SDK)](appx-packaging-samples.md)                                                                | téléchargez les exemples du kit de développement logiciel (SDK) qui illustrent le packaging, le déploiement et les api de requête des applications Windows.                                                                               |
| [Glossaire](appx-packaging-glossary.md)                                                                  | en savoir plus sur les termes liés à l’empaquetage, au déploiement et à l’interrogation des applications Windows.                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Concepts**
</dt> <dt>

[Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Autre référence**
</dt> <dt>

[Schéma de manifeste du package de l’application](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel. PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 