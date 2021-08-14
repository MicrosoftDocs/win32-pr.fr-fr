---
description: L’événement InkOverlay. NewInAirPackets-se produit lorsqu’un paquet in-air est détecté.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: InkOverlay. NewInAirPackets, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198fe2d105421654bfba037049e46a592d603bd94409350e97b794882ab4de2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219167"
---
# <a name="inkoverlaynewinairpackets-event"></a>Événement InkOverlay. NewInAirPackets

Se produit lorsqu’un paquet air est détecté.

## <a name="syntax"></a>Syntaxe


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkcollector-newinairpackets.md) .

</dd> <dt>

*PacketCount* \[ dans\]
</dt> <dd>

Nombre de paquets in-air reçus.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Tableau qui contient les données sélectionnées pour le paquet.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Un paquet aérien est créé lorsqu’un utilisateur déplace un stylet près de la tablette et que le curseur se trouve dans la fenêtre de l’objet du collecteur d’encre ou lorsque l’utilisateur déplace une souris dans la fenêtre associée de l’objet du collecteur. Les événements [**NewInAirPackets**](inkcollector-newinairpackets.md) sont générés rapidement et le gestionnaire d’événements doit être rapide ou en pâtit d’une performance.

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICENewInAirPackets.

L’événement [**NewInAirPackets**](inkcollector-newinairpackets.md) est déclenché même en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

Pour définir les propriétés contenues dans ce tableau, utilisez la propriété [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) de l’objet Ink collector. Le tableau retourné par le paramètre *PacketData* contient les données de ces propriétés.

> [!Note]  
> Bien que vous puissiez modifier les données du paquet, ces modifications ne sont pas conservées ou utilisées.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[**Propriété DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Événement NewPackets**](inkcollector-newpackets.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




