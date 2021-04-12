---
description: Se produit lorsque le collecteur d’encres reçoit un paquet.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Événement InkCollector. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b03e1a561a61c9b291bca8e59f990dc12b4e2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318101"
---
# <a name="inkcollectornewpackets-event"></a>Événement InkCollector. NewPackets

Se produit lorsque le collecteur d’encres reçoit un paquet.

## <a name="syntax"></a>Syntaxe


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkcollector-newinairpackets.md) .

</dd> <dt>

*Trait* \[ dans\]
</dt> <dd>

Spécifie l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketCount* \[ dans\]
</dt> <dd>

Nombre de paquets reçus pour un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Lorsque cette méthode est retournée, contient un tableau qui contient les données sélectionnées pour le paquet.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les paquets sont reçus lorsqu’un trait est collecté. Les événements de paquets se produisent rapidement et un gestionnaire d’événements **NewPackets** doit être rapide ou subir des performances.

La méthode d’événement TCet est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IINKPICTUREEVENTS avec l’ID DISPID \_ ICENewPackets.

Cet événement doit être utilisé avec précaution, car il peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements.

Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) de l’objet Ink collector. Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.

> [!Note]  
> Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkCollector (classe)**](inkcollector-class.md)
</dt> <dt>

[**Événement NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




