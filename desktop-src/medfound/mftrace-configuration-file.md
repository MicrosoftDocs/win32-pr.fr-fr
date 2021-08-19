---
description: L’outil MFTrace peut lire un fichier de configuration XML qui spécifie un ou plusieurs fournisseurs de suivi.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Fichier de configuration MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871936"
---
# <a name="mftrace-configuration-file"></a>Fichier de configuration MFTrace

L’outil [MFTrace](mftrace.md) peut lire un fichier de configuration XML qui spécifie un ou plusieurs fournisseurs de suivi.

L’élément [**providers**](providers.md) est l’élément racine dans le fichier de configuration.

## <a name="in-this-section"></a>Dans cette section

-   [**mot**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**moteur**](provider.md)
-   [**fournisseurs**](providers.md)

## <a name="example"></a>Exemples

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

 

 



