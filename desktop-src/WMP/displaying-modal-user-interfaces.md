---
title: Affichage des interfaces utilisateur modales
description: Affichage des interfaces utilisateur modales
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Plug-ins du lecteur Windows Media, affichage des boîtes de dialogue et des messages
- plug-ins, affichage des boîtes de dialogue et des messages
- plug-ins d’interface utilisateur, affichage de boîtes de dialogue et de messages
- Plug-ins d’interface utilisateur, affichage des boîtes de dialogue et des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675885"
---
# <a name="displaying-modal-user-interfaces"></a>Affichage des interfaces utilisateur modales

Les plug-ins de l’interface utilisateur ne doivent pas afficher de boîtes de dialogue modales ou de messages en réponse aux appels de méthode du lecteur Windows Media. Par exemple, n’affichez pas de boîte de message à partir de votre implémentation de **IWMPPluginUI :: Create**.

Si vous devez afficher une boîte de dialogue ou une boîte de message à partir d’une implémentation de méthode de plug-in d’interface utilisateur qui est appelée par le lecteur, vous devez effectuer les étapes suivantes :

1.  Inscrire un nouveau message de fenêtre à l’aide de **RegisterWindowMessage**.
2.  Envoyez le message de fenêtre que vous avez enregistré dans votre fenêtre de plug-in d’interface utilisateur à l’aide de **PostMessage**.
3.  Affichez la boîte de dialogue ou la boîte de message à partir du gestionnaire de messages pour votre nouveau message de fenêtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble du plug-in d’interface utilisateur**](ui-plug-in-overview.md)
</dt> </dl>

 

 




