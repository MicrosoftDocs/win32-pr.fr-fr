---
title: Développement d’applications pour les versions antérieures de Windows
description: Explique ce que vous devez faire pour développer des applications qui s’exécutent sur des versions antérieures de Windows et tirer parti de l’API prise en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393891"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Développement d’applications pour les versions antérieures de Windows

Explique ce que vous devez faire pour développer des applications qui s’exécutent sur des versions antérieures de Windows et tirer parti de l’API prise en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.

## <a name="required-downloads"></a>Téléchargements requis

Le téléchargement et l’installation des packages décrits dans les sections suivantes sont nécessaires si vous souhaitez développer des applications qui utilisent des API introduites avec le kit de développement logiciel (SDK) Microsoft Windows pour Windows 7.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

La SDK Windows pour Windows 7 est nécessaire pour créer des applications qui utilisent des API prises en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.

Pour accéder à des ressources et des informations supplémentaires, telles que des téléchargements, des publications de forum et le blog de l’équipe SDK Windows, consultez le [Centre de développement SDK Windows](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Le .NET Framework 3,5 Service Pack 1 est requis pour créer des applications qui utilisent des API prises en charge par la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.

Pour obtenir des informations et des ressources supplémentaires, consultez le [Centre de développement .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>SDK DirectX requis lors de l’utilisation de Direct3D

Si vous créez des applications qui utilisent Direct3D, le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) est requis pour créer des applications qui utilisent des API prises en charge par la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.

### <a name="update-your-development-computer"></a>Mettre à jour votre ordinateur de développement

Assurez-vous que votre ordinateur de développement dispose de toutes les mises à jour les plus récentes à partir de Windows Update.

Si vous développez des applications sur une version antérieure de Windows, vous devez obtenir la mise à jour de la plateforme pour Windows Vista ou la mise à jour de la plateforme pour Windows Server 2008 à partir de Windows Update. L’installation de l’une de ces mises à jour vous permettra de tirer parti de la nouvelle API fournie par le SDK Windows pour Windows 7.

Pour plus d’informations sur la façon d’obtenir des mises à jour à partir de Windows Update consultez l' [article de la base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Environnement de développement

### <a name="set-the-build-target-to-windows-7"></a>Définir la cible de génération sur Windows 7

Toutes les applications qui utilisent des bibliothèques dans la mise à jour de plateforme pour Windows Vista doivent être générées par rapport à la plateforme cible Windows 7.

La définition de WINVER sur la valeur de la plateforme cible Windows 7 vous permet de développer des applications qui utilisent des API prises en charge avec la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008 sur un ordinateur de développement exécutant Windows Vista.

Vous pouvez définir la plateforme cible sur Windows 7 dans votre code source ou à l’aide de l’option/D avec le compilateur Visual Studio.

L’exemple suivant montre comment définir WINVER dans votre code source.


```C++
#define WINVER 0x0601
```



L’exemple suivant montre comment définir WINVER à l’aide de l’option du compilateur/D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Déploiement d’application

Si vous générez votre application à l’aide des en-têtes et des bibliothèques fournis par le SDK Windows pour Windows 7, les API prises en charge s’exécuteront sur toutes les versions de Windows dont la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008 est installée.

> [!Note]  
> Le comportement, les performances ou la configuration requise pour certaines API prises en charge avec la mise à jour de plateforme pour Windows Vista ou pour la mise à jour de plateforme pour Windows Server 2008 peuvent varier selon les différentes versions de Windows. Pour plus d’informations sur une API spécifique prise en charge par les mises à jour, consultez à [propos de la mise à jour de la plateforme pour Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Aucun composant redistribuable

Votre application n’a pas besoin d’installer des composants redistribuables, tels que des dll ou d’autres fichiers d’exécution.

### <a name="requires-updated-end-user-computer"></a>Nécessite la mise à jour de End-User ordinateur

Étant donné que la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 sont hébergées par Windows Update, les utilisateurs finaux avec des mises à jour automatiques activées sont très susceptibles d’avoir déjà ces mises à jour, ainsi que les service packs requis.

Si l’ordinateur de l’utilisateur final ne dispose pas de la mise à jour de la plateforme pour Windows Vista ou de la mise à jour de la plateforme pour Windows Server 2008 et que votre application nécessite des API prises en charge avec ces mises à jour, il se peut que votre application ne puisse pas s’exécuter sur l’ordinateur de l’utilisateur final ou rencontre des erreurs lors de son exécution.

Pour éviter les problèmes qui peuvent être causés par l’ordinateur de l’utilisateur obsolète, vous devez vérifier que l’ordinateur de l’utilisateur dispose de la mise à jour de la plateforme pour Windows Vista ou de la mise à jour de la plateforme pour Windows Server 2008 lors de l’installation de votre application. Vous pouvez utiliser l' [API](/windows/desktop/Wua_Sdk/portal-client) de l’Agent de Windows Update pour vérifier l’ordinateur de l’utilisateur final pour les mises à jour installées. Vous pouvez également utiliser l’API Windows Update Agent pour télécharger et installer les mises à jour requises lors de l’installation de l’application si l’utilisateur final n’a pas déjà installé les mises à jour.

Pour obtenir un exemple de programme d’installation qui montre comment utiliser l’API de l' [agent de Windows Update](/windows/desktop/Wua_Sdk/portal-client), consultez [déploiement de Direct3D 11 pour les développeurs de jeux](../direct3darticles/direct3d11-deployment.md) dans le kit de [développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Bien que l’exemple de programme d’installation D3D11InstallHelper abordé dans le [déploiement de Direct3D 11 pour les développeurs de jeux](../direct3darticles/direct3d11-deployment.md)ait été conçu pour les applications qui utilisent Direct3D 11, il fournit un bon exemple d’interaction avec l' [API d’agent Windows Update](/windows/desktop/Wua_Sdk/portal-client) pour lancer et suivre le téléchargement et l’installation des mises à jour qui sont hébergées par Windows Update. La compilation de cet exemple peut nécessiter l’SDK Windows pour Windows 7. Pour plus d’informations sur l’exemple D3D11InstallHelper, y compris les problèmes connus, consultez le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notes de publication pour août 2009. mise à jour de la plateforme pour Windows Vista

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise à jour de plateforme pour Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Vues d'ensemble**
</dt> <dt>

[À propos de la mise à jour de plateforme pour Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Article de la base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 