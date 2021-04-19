---
description: L’outil MFTrace peut lire un fichier de configuration XML qui spécifie un ou plusieurs fournisseurs de suivi.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Fichier de configuration MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529769"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="7fb50-103">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="7fb50-103">MFTrace Configuration File</span></span>

<span data-ttu-id="7fb50-104">L’outil [MFTrace](mftrace.md) peut lire un fichier de configuration XML qui spécifie un ou plusieurs fournisseurs de suivi.</span><span class="sxs-lookup"><span data-stu-id="7fb50-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="7fb50-105">L’élément [**providers**](providers.md) est l’élément racine dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="7fb50-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7fb50-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7fb50-106">In this section</span></span>

-   [<span data-ttu-id="7fb50-107">**keyword**</span><span class="sxs-lookup"><span data-stu-id="7fb50-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="7fb50-108">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="7fb50-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="7fb50-109">**moteur**</span><span class="sxs-lookup"><span data-stu-id="7fb50-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="7fb50-110">**fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="7fb50-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="7fb50-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="7fb50-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="7fb50-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fb50-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb50-113">MFTrace</span><span class="sxs-lookup"><span data-stu-id="7fb50-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



