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
# <a name="mftrace-configuration-file"></a>Fichier de configuration MFTrace

L’outil [MFTrace](mftrace.md) peut lire un fichier de configuration XML qui spécifie un ou plusieurs fournisseurs de suivi.

L’élément [**providers**](providers.md) est l’élément racine dans le fichier de configuration.

## <a name="in-this-section"></a>Dans cette section

-   [**keyword**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**moteur**](provider.md)
-   [**fournisseurs**](providers.md)

## <a name="example"></a>Exemple

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 



