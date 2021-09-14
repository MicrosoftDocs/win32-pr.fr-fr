---
title: Types signés et non signés (MIDL)
description: En savoir plus sur les types signés et non signés dans MIDL. Les compilateurs qui utilisent différents types par défaut peuvent provoquer des erreurs logicielles dans votre application distribuée.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- types de données MIDL, signés et non signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093197"
---
# <a name="signed-and-unsigned-types-midl"></a>Types signés et non signés (MIDL)

Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée. Vous pouvez éviter ces problèmes en déclarant explicitement vos types de caractères comme étant signés ou non signés. Notez que les compilateurs IDL DCE ne reconnaissent pas le mot clé [**signed**](signed.md). Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur/**OSF** du compilateur MIDL.

MIDL définit le [**petit**](small.md) type pour qu’il prenne le même signe par défaut que le type [**char**](char-idl.md) dans le compilateur C cible. Si le compilateur suppose que **char** n’est pas signé, **Small** sera également défini comme non signé. De nombreux compilateurs C vous permettent de modifier la valeur par défaut en tant qu’option de ligne de commande. par exemple, dans l’environnement de développement Microsoft Visual C++, l’option de ligne de commande **/j** modifie la signature par défaut de **char** de signed en non signé.

Vous pouvez également contrôler le signe des variables de type [**char**](char-idl.md) et [**Small**](small.md) avec le commutateur de ligne de commande du compilateur MIDL [**/char**](-char.md). Ce commutateur vous permet de spécifier le signe par défaut utilisé par votre compilateur. Le compilateur MIDL déclare explicitement le signe de tous les types **char** qui ne correspondent pas à votre type par défaut du compilateur C dans le fichier d’en-tête généré.

 

 




