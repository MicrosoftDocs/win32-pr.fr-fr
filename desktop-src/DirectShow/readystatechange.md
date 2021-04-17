---
description: L’événement ReadyStateChange est envoyé lorsque la propriété ReadyState du contrôle MSWebDVD a été modifiée.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522047"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

L' `ReadyStateChange` événement est envoyé lorsque la propriété **ReadyState** du contrôle mswebdvd a changé.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*DataControl*
</dt> <dd>

Spécifie la nouvelle valeur de la propriété [**ReadyState**](readystate-property.md) .



| Valeur | Description               |
|-------|---------------------------|
| 0     | READYSTATE \_ non initialisé |
| 1     | chargement de READYSTATE \_       |
| 2     | READYSTATE \_ chargé        |
| 3     | \_interactive ReadyState   |
| 4     | READYSTATE \_ terminé      |



 

</dd> </dl>

 

 



