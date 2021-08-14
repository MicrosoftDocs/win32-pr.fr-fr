---
description: Formats d’extension MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formats d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193955"
---
# <a name="mtp-extension-formats"></a>Formats d’extension MTP

Le format d’un fichier sur un appareil peut être décrit par une valeur GUID. Cette valeur est spécifiée par la \_ propriété format de l’objet wpd \_ .

## <a name="vendor-extended-formats"></a>Formats étendus par le fournisseur

Quand un fabricant de périphériques prend en charge un format étendu de fournisseur, son pilote associe le code de format du fournisseur (UINT16) avec les 16 bits les plus élevés du **\_ format d’objet wpd \_ \_ non spécifié** .

Par exemple, si le code étendu du fournisseur est 0xB001, le GUID résultant est comme indiqué dans l’exemple suivant :


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des extensions MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



