---
title: Type-Conversion et marshaling des attributs ACF
description: Utilisez ces attributs pour contrôler la façon dont vos données sont transmises sur le réseau.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL, attributs, conversion de type et marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286de08a56aba5ffc7b73fc52791238a6af62b3f0545e95aedabcf79d5623464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382731"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion et marshaling des attributs ACF

Utilisez ces attributs pour contrôler la façon dont vos données sont transmises sur le réseau.



| Attribut                                        | Usage                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**coder**](encode.md)le [**décode**](decode.md) | Ordonne à MIDL d’exposer les routines de sérialisation de type ou de procédure qu’il génère pour les stubs. Votre application cliente peut appeler ces routines pour marshaler les données par valeur.                                                                                                                                                                                                                                                                                  |
| [**représenter \_ comme**](represent-as.md)            | Spécifie la manière dont un type de données est représenté sur le câble, lorsque la nature exacte du type de données d’un client n’a pas d’importance pour le serveur (parce qu’il n’a besoin que des données elles-mêmes et non de la structure réelle), ou que le type de client réel est inconnu de MIDL au moment de la compilation. Par exemple, si votre application cliente utilise une liste liée de nombres à virgule flottante, vous pouvez spécifier que la représentation filaire de cette liste soit un tableau de type [**float**](float.md). |
| [**Marshal d’utilisateur \_**](user-marshal.md)            | Contrôle la façon dont les données sont transmises sur le réseau en implémentant vos propres routines de marshaling. Cet attribut est utile si vous avez un type de données inconnu pour MIDL ou si vous transmettez des informations entre des plateformes Big-endian et Little-endian.                                                                                                                                                                                                                 |



 

Les attributs de marshaling DCE [**en \_ ligne**](in-line.md) et [**hors \_ \_ ligne**](out-of-line.md) ne sont pas implémentés dans Microsoft RPC. Le compilateur MIDL marshale automatiquement les types de données complexes hors ligne.

 

 




