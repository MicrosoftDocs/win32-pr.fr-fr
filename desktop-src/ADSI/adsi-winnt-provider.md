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
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379599"
---
# <a name="adsi-winnt-provider"></a>Fournisseur WinNT ADSI

Le fournisseur Microsoft ADSI implémente un ensemble d’objets ADSI pour prendre en charge différentes interfaces ADSI. Le nom de l’espace de noms pour le fournisseur Windows est « Winnt » et ce fournisseur est communément appelé le fournisseur Winnt. Pour accéder au fournisseur WinNT, établissez une liaison à l’un des [objets ADSI de Winnt](adsi-objects-of-winnt.md)à l’aide de la valeur [ADsPath de Winnt](winnt-adspath.md).

Le fournisseur Winnt est inclus dans le composant système ADSI pour Windows et Windows Server.

> [!Note]  
> Le fournisseur Winnt par défaut ne peut pas être considéré comme entièrement thread-safe. Les Writers d’applications multithread doivent gérer le multithreading pour coordonner correctement tout accès entre les threads via l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.

 

 

 




