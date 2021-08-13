---
description: Le champ de longueur dans un tripleon TLV identifie le nombre d’octets encodés dans le champ de valeur.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Octets de longueur et de valeur encodés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44ec9892e9407cbe587dbb60219b758ac95392e64dfabcf4866e02a1ad9343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904472"
---
# <a name="encoded-length-and-value-bytes"></a>Octets de longueur et de valeur encodés

Le champ de *longueur* dans un tripleon TLV identifie le nombre d’octets encodés dans le champ de *valeur* . Le champ *valeur* contient le contenu envoyé entre les ordinateurs. Si le champ de *valeur* contient moins de 128 octets, le champ de *longueur* ne requiert qu’un octet. Le bit 7 du champ de *longueur* est égal à zéro (0) et les bits restants identifient le nombre d’octets de contenu à envoyer. Si le champ de *valeur* contient plus de 127 octets, le bit 7 du champ de *longueur* est un (1) et les bits restants identifient le nombre d’octets nécessaires pour contenir la longueur. Les exemples sont présentés dans l’illustration suivante.

![octet de longueur der TLV](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de transfert DER](about-der-transfer-syntax.md)
</dt> <dt>

[Octets de balise encodés](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



