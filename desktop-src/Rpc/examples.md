---
title: Exemples (RPC)
description: Exemples qui illustrent les concepts de l’appel de procédure distante (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Appel de procédure distante RPC, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930048"
---
# <a name="examples-rpc"></a>Exemples (RPC)

Le kit de développement logiciel (SDK) de la plateforme contient des exemples qui illustrent un grand nombre de concepts de l’appel de procédure distante (RPC), comme suit :

-   ASYNCRPC illustre la structure d’une application RPC qui utilise des appels de procédure distante asynchrones. Il montre également différentes méthodes de notification de la fin de l’appel.
-   CLUUID illustre l’utilisation de l’UUID de l’objet client pour permettre à un client de sélectionner plusieurs implémentations d’une procédure distante.
-   Le répertoire de données contient quatre programmes : DUNION illustre les unions discriminées (qui ne sont pas encapsulées). INOUT montre [ \[ dans \] ](../midl/in.md), [ \[ les \] paramètres out](../midl/out-idl.md) ; REPAS montre l’attribut [dereprésente \_ comme](/windows/desktop/Midl/represent-as) Attribute ; La transmission illustre l’attribut [transmit \_ As](/windows/desktop/Midl/transmit-as) .
-   DYNEPT illustre une application cliente qui gère sa connexion au serveur via des points de terminaison dynamiques.
-   Le répertoire FILEREP contient quatre exemples illustrant comment les développeurs peuvent écrire un service de réplication de fichiers simple, un service de réplication de fichiers multi-utilisateur, un service prenant en charge les fonctionnalités de sécurité et un service utilisant des canaux RPC asynchrones.
-   Le répertoire HANDles contient trois programmes, AUTO, CXHNDL, USRDEF, qui illustrent respectivement le descripteur [automatique \_ ](/windows/desktop/Midl/auto-handle), le \[ handle de contexte \_ \] et les handles génériques (définis par l’utilisateur).
-   HELLO est une implémentation client/serveur de « Hello, World ».
-   Le répertoire PICKLE contient deux programmes : PICKLP illustre la sérialisation des procédures de données ; La liste déroulante illustre la sérialisation des types de données. les deux programmes utilisent les attributs [ \[ encode \] ](../midl/encode.md) et [ \[ Decode \] ](../midl/decode.md) .
-   Les canaux illustrent l’utilisation du constructeur de type pipe.
-   RPCSVC illustre l’implémentation d’un service avec RPC.
-   STROUT montre comment allouer de la mémoire sur un serveur pour un objet à deux dimensions (un tableau de pointeurs) et le retourner au client en tant \[ que \] paramètre en sortie seule. Le client libère ensuite la mémoire. Cette technique permet au stub d’appeler le serveur sans savoir à l’avance la quantité de données qui sera retournée.

    Ce programme permet également à l’utilisateur d’effectuer une compilation pour UNICODE ou ANSI.

Tous les fichiers sources et makefiles pour ces programmes se trouvent dans le kit de développement logiciel (SDK) de plateforme.

Pour un développement d’applications RPC de base et des exemples plus simples, consultez les rubriques du [didacticiel](tutorial.md) .

 

 
