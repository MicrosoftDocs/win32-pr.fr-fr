---
title: Couche de compatibilité des applications
description: Pour exécuter des applications héritées dans un environnement Services Bureau à distance, vous pouvez utiliser la couche de compatibilité des applications Services Bureau à distance.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511704"
---
# <a name="application-compatibility-layer"></a>Couche de compatibilité des applications

Pour exécuter des applications héritées dans un environnement Services Bureau à distance, vous pouvez utiliser la couche de compatibilité des applications Services Bureau à distance. Lorsque le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) charge une application qui n’est pas Services Bureau à distancee en charge, il charge également une DLL qui contient le code de compatibilité. Pour utiliser la couche de compatibilité des applications Services Bureau à distance, vous pouvez définir l’indicateur NOT TSAWARE lors de la compilation d’une application.

Si votre application ne prend Services Bureau à distance en charge, vous pouvez éviter la surcharge liée au chargement de cette DLL supplémentaire et à l’exécution du code de compatibilité.

Pour indiquer que votre application n’est Services Bureau à distance prise en charge, définissez l’indicateur de prise en **\_ \_ charge de terminal \_ Server \_ de l’image DLLCHARACTERISTICS** dans l’en-tête facultatif. Si vous utilisez l’éditeur de liens fourni avec Microsoft Visual C++, vous pouvez utiliser l’option de l’éditeur de liens **TSAWARE** pour définir cet indicateur. L’outil **DUMPBIN** fourni avec Microsoft Visual C++ fournit l’option */headers* pour déterminer l’état de l’indicateur **TSAWARE** . Pour plus d’informations sur l’utilisation de l’outil **DUMPBIN** , consultez [Référence DUMPBIN](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Soyez prudent lorsque vous utilisez l’indicateur **TSAWARE** , car il permet à votre application de contourner toutes les optimisations de compatibilité services Bureau à distance. L’indicateur **TSAWARE** doit être utilisé uniquement si vous êtes certain que votre application est conçue pour l’environnement services Bureau à distance. Si votre application répond aux critères suivants, vous pouvez utiliser en toute sécurité l’indicateur de **reconnaissance d’image \_ DLLCHARACTERISTICS \_ Terminal \_ Server \_** .

-   L’application n’utilise pas de fichiers. ini.
-   L’application n’écrit pas dans **HKEY \_ Current \_ User** lors de l’installation. Pour plus d’informations, consultez [stockage des informations de User-Specific](storing-user-specific-information.md).
-   L’application ne s’exécute pas en tant que service système (c’est-à-dire LUID = System).
-   L’application n’attend pas l’accès exclusif aux répertoires Windows ou aux autres répertoires système. Cela signifie que l’application ne stocke pas les données temporaires ou de configuration par utilisateur dans les répertoires système Windows ou autres.
-   L’application n’écrit pas dans la ruche de Registre **HKEY local machine** pour la configuration ou les données spécifiques à l’utilisateur.
-   L’application suit les autres instructions de compatibilité Services Bureau à distance mentionnées dans ce document.

 

 