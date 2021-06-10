---
title: Énumération des ressources
description: Cette rubrique décrit les fonctions utilisées pour obtenir des listes de ressources.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910265"
---
# <a name="enumerating-resources"></a>Énumération des ressources

Dans certaines situations, vous souhaiterez peut-être découvrir le contenu des ressources d’un module exécutable portable (PE) inconnu. Le SDK Windows fournit des fonctions d’énumération des ressources qui permettent à votre application d’obtenir des listes de types de ressources, de noms et de langages dans un module spécifié.

* Les fonctions [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) et [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) fournissent une liste des types de ressources trouvés dans le module.
* Les fonctions [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) et [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) fournissent le nom de chaque ressource dans un type donné.
* Les fonctions [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) et [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) fournissent le langage de chaque ressource d’un nom et d’un type donnés. 

Ces fonctions et leurs fonctions de rappel associées permettent à votre application de créer une liste de toutes les ressources dans un module. Ce processus est décrit dans [création d’une liste de ressources](using-resources.md).

## <a name="-see-also"></a>-Voir-aussi

[ Exemple d’applicationMsistuff.exe](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
