---
title: Fournisseur WinNT ADSI
description: Le fournisseur Microsoft ADSI implémente un ensemble d’objets ADSI pour prendre en charge différentes interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI du fournisseur Winnt ADSI
- ADSI du fournisseur de services Winnt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692789"
---
# <a name="adsi-winnt-provider"></a>Fournisseur WinNT ADSI

Le fournisseur Microsoft ADSI implémente un ensemble d’objets ADSI pour prendre en charge différentes interfaces ADSI. le nom de l’espace de noms pour le fournisseur de Windows est « winnt » et ce fournisseur est communément appelé le fournisseur winnt. Pour accéder au fournisseur WinNT, établissez une liaison à l’un des [objets ADSI de Winnt](adsi-objects-of-winnt.md)à l’aide de la valeur [ADsPath de Winnt](winnt-adspath.md).

le fournisseur winnt est inclus dans le composant système ADSI pour Windows et Windows Server.

> [!Note]  
> Le fournisseur Winnt par défaut ne peut pas être considéré comme entièrement thread-safe. Les Writers d’applications multithread doivent gérer le multithreading pour coordonner correctement tout accès entre les threads via l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.

 

 

 




