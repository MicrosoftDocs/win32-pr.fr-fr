---
description: Le fragment de code suivant illustre la modification d’un intervalle de temps de conférences. L’intervalle de temps par défaut est de trente minutes. Dans ce fragment, l’intervalle de temps est défini sur une année.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modification d’une conférence connue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201205"
---
# <a name="modifying-a-known-conference"></a>Modification d’une conférence connue

\[Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le fragment de code suivant illustre la modification de l’intervalle de temps d’une conférence. L’intervalle de temps par défaut est de trente minutes. Dans ce fragment, l’intervalle de temps est défini sur une année.

Ce fragment suppose que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée et qu’une [énumération de répertoires de conférence](enumerating-conference-directories.md) a été effectuée pour obtenir l’entrée d’annuaire qui sera modifiée.

Ce fragment suppose également qu’il ne s’agit pas d’une conférence multidiffusion. La modification des heures d’une conférence multidiffusion requiert la notification du serveur d’allocation d’adresses de multidiffusion. Pour obtenir un exemple d’utilisation de l’adressage de multidiffusion, consultez [acquisition d’une adresse de multidiffusion](acquiring-a-multicast-address.md) .


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



