---
title: VBRPeak
description: L’attribut VBRPeak contient le taux binaire le plus élevé dans un flux encodé VBR (variable bit rate).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Format Windows Media VBRPeak
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030328"
---
# <a name="vbrpeak"></a>VBRPeak

L’attribut **VBRPeak** contient le taux binaire le plus élevé dans un flux encodé VBR (variable bit rate).

## <a name="global-constant"></a>Constante globale

\_wszVBRPeak g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur. Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.

Le writer écrit automatiquement une valeur **VBRPeak** pour chaque flux VBR.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




