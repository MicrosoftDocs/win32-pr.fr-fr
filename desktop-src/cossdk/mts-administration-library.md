---
description: La bibliothèque d’administration MTS fournie avec les interfaces d’administration COM+ offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Bibliothèque d’administration MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523540"
---
# <a name="mts-administration-library"></a>Bibliothèque d’administration MTS

La bibliothèque d’administration MTS fournie avec les interfaces d’administration COM+ offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0. La plupart des codes d’administration MTS 2,0 existants fonctionnent toujours avec la bibliothèque MTSAdmin fournie. Toutefois, certaines fonctionnalités ont changé.

Pour tirer parti de nouvelles fonctionnalités ou si vous écrivez du code d’administration pour la première fois, vous devez utiliser la bibliothèque comadmin.

Les éléments suivants de la bibliothèque d’administration MTS actuelle sont modifiés à partir de la bibliothèque d’administration MTS 2,0 :

-   L’interface **IRemoteComponentUtil** n’est plus disponible.
-   La collection **RemoteComponents** n’est plus disponible.
-   La propriété RoleID n’est plus disponible, le nom de rôle est maintenant utilisé comme clé pour ce.
-   La méthode **ExportPackage** n’exporte plus de client.exe.
-   La propriété RemoteComponentInstallPath n’est plus exposée sur la collection [**LocalComputer**](localcomputer.md) .
-   La propriété ApplicationInstallPath ne sera plus exposée sur la collection [**LocalComputer**](localcomputer.md) .
-   Le package système est maintenant nommé application système.
-   Le package Utilities est maintenant nommé utilitaires COM+.
-   La propriété IsSystem existe dans la collection de [**composants**](components.md) dans MTSAdmin, mais retourne « NotImpl » quand elle est activée et n’est pas enregistrée si elle est définie.
-   La propriété PackageName n’est plus prise en charge par la collection de [**composants**](components.md) . Pour déterminer le nom du package, vous devez maintenant obtenir le PackageID, puis rechercher le package correspondant dans la collection de packages.
-   Les propriétés suivantes n’existent plus sur la collection [**InterfacesForComponent**](interfacesforcomponent.md) :
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion automatique à partir de MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Résultats et problèmes de conversion COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversion manuelle à partir de MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



