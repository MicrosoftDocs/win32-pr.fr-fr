---
title: Types signés et non signés (RPC)
description: En savoir plus sur les types signés et non signés dans RPC. Les compilateurs qui utilisent différents types par défaut peuvent provoquer des erreurs logicielles dans votre application distribuée.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17a2ccf28233bb14e0811e8015c83aede37d60c58fe9411f13806355fdb7f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017696"
---
# <a name="signed-and-unsigned-types-rpc"></a>Types signés et non signés (RPC)

Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée. Vous pouvez éviter ces problèmes en déclarant explicitement vos types de caractères comme étant **signés** ou **non signés**.

MIDL définit le [**petit**](/windows/desktop/Midl/small) type pour qu’il prenne le même signe par défaut que le type **char** dans le compilateur C cible. Si le compilateur suppose que **char** n’est pas signé, **Small** sera également défini comme non signé. De nombreux compilateurs C vous permettent de modifier la valeur par défaut en tant qu’option de ligne de commande. Par exemple, l’option de ligne de commande de Microsoft C compiler **/j** change la signature par défaut de **char** de signed en non signé.

Vous pouvez également contrôler le signe des variables de type **char** et **Small** avec le commutateur de ligne de commande du compilateur MIDL [**/char**](/windows/desktop/Midl/-char). Ce commutateur vous permet de spécifier le signe par défaut utilisé par votre compilateur. Le compilateur MIDL déclare explicitement le signe de tous les types **char** qui ne correspondent pas à votre type par défaut du compilateur C dans le fichier d’en-tête généré.

 

 
