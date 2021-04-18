---
description: L’outil unlodctr supprime les entrées de Registre créées par lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Suppression des noms et des descriptions des compteurs du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519897"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Suppression des noms et des descriptions des compteurs du Registre

L’outil **unlodctr** supprime les entrées de Registre créées par **lodctr**. Le nom de l’application que vous transmettez à **unlodctr** doit correspondre au [nom de la clé d’application](creating-the-applications-performance-key.md) que vous avez créée sous la clé **services** . Pour plus d’informations sur l’exécution de **unlodctr** , consultez le centre d’aide et de support.

## <a name="using-unlodctr"></a>Utilisation de unlodctr

L’outil **unlodctr** recherche le premier et le dernier compteur et aide à indexer les valeurs à l’aide des valeurs de Registre similaires, sous la clé de **performances** de votre application. L’outil **unlodctr** utilise la plage de valeurs d’index pour supprimer le texte des **compteurs** et des valeurs d' **aide** pour chaque identificateur de langue.

À l’aide des valeurs d’index, **unlodctr** apporte les modifications suivantes au registre.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

L’outil **unlodctr** supprime également les valeurs du **premier compteur**, du **dernier compteur**, de la **première aide**, de la **dernière aide** et de la **liste d’objets** de la clé de **performance** de l’application située dans **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **services** \\ *application-name* \\ **performance**.

> [!Note]  
> La fonction de déchargement de **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), est déclarée dans loadperf. h et exportée à partir de Loadperf.dll. Cela vous permet d’appeler cette fonction directement à partir de votre programme de désinstallation.

 

 

 



