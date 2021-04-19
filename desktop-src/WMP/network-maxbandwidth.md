---
title: Network. maxBandwidth
description: La propriété maxBandwidth spécifie ou récupère la bande passante maximale autorisée.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Lecteur Windows Media Network. maxBandwidth
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539502"
---
# <a name="networkmaxbandwidth"></a>Network. maxBandwidth

La propriété **maxBandwidth** spécifie ou récupère la bande passante maximale autorisée.

## <a name="syntax"></a>Syntaxe

*lecteur*. *réseau*. **maxBandwidth**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**).

## <a name="remarks"></a>Notes

Cette propriété n’a aucune valeur par défaut. Sa valeur peut être spécifiée pendant la lecture du lecteur Windows Media, mais la modification ne prendra effet qu’après la libération de l’élément multimédia en cours en ouvrant un autre élément ou en appelant le *lecteur*. **Fermez**. Le lecteur Windows Media tente d’obtenir la bande passante la plus élevée possible. Une réduction de la bande passante se produit uniquement dans le cas de la valeur définie.

Ce paramètre est utile pour réduire la quantité de bande passante utilisée, en particulier dans le cas d’un flux de la vitesse de transmission multiple (MBR). Un flux MBR contient plusieurs flux avec différentes vitesses de transmission. Dans certains cas, il peut être souhaitable d’utiliser un flux avec une vitesse de transmission inférieure à celle requise par le client. Dans ce cas, la définition de la propriété **maxBandwidth** sélectionnera un flux de vitesse de transmission inférieur.

Par exemple, un flux de données MBR peut inclure des flux encodés à 20 kilobits par seconde (Kbits/s), 37 Kbits/s et 200 kbit/s. Si vous affectez à la propriété **maxBandwidth** la valeur 50 000 (50 Kbits/s), vous sélectionnez le flux de 37 kbps au lieu du flux de 200 Kbits/s.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





