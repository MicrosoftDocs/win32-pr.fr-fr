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
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="0c8d1-103">Suppression des noms et des descriptions des compteurs du Registre</span><span class="sxs-lookup"><span data-stu-id="0c8d1-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="0c8d1-104">L’outil **unlodctr** supprime les entrées de Registre créées par **lodctr**.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="0c8d1-105">Le nom de l’application que vous transmettez à **unlodctr** doit correspondre au [nom de la clé d’application](creating-the-applications-performance-key.md) que vous avez créée sous la clé **services** .</span><span class="sxs-lookup"><span data-stu-id="0c8d1-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="0c8d1-106">Pour plus d’informations sur l’exécution de **unlodctr** , consultez le centre d’aide et de support.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="0c8d1-107">Utilisation de unlodctr</span><span class="sxs-lookup"><span data-stu-id="0c8d1-107">Using unlodctr</span></span>

<span data-ttu-id="0c8d1-108">L’outil **unlodctr** recherche le premier et le dernier compteur et aide à indexer les valeurs à l’aide des valeurs de Registre similaires, sous la clé de **performances** de votre application.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="0c8d1-109">L’outil **unlodctr** utilise la plage de valeurs d’index pour supprimer le texte des **compteurs** et des valeurs d' **aide** pour chaque identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="0c8d1-110">À l’aide des valeurs d’index, **unlodctr** apporte les modifications suivantes au registre.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

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

<span data-ttu-id="0c8d1-111">L’outil **unlodctr** supprime également les valeurs du **premier compteur**, du **dernier compteur**, de la **première aide**, de la **dernière aide** et de la **liste d’objets** de la clé de **performance** de l’application située dans **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **services** \\ *application-name* \\ **performance**.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="0c8d1-112">La fonction de déchargement de **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), est déclarée dans loadperf. h et exportée à partir de Loadperf.dll.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="0c8d1-113">Cela vous permet d’appeler cette fonction directement à partir de votre programme de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="0c8d1-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



