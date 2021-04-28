---
description: L’événement InkPicture. NewPackets-se produit lorsque le collecteur d’encres reçoit un paquet.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: InkPicture. NewPackets, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086477"
---
# <a name="inkpicturenewpackets-event"></a>InkPicture. NewPackets, événement

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

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**NewInAirPackets**](inkpicture-newinairpackets.md) .

</dd> <dt>

*Trait* \[ dans\]
</dt> <dd>

Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketCount* \[ dans\]
</dt> <dd>

Nombre de paquets reçus pour un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Tableau qui contient les données sélectionnées pour le paquet.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Les paquets sont reçus lorsqu’un trait est collecté. Les événements de paquets se produisent rapidement et un gestionnaire d’événements **NewPackets** doit être rapide ou subir des performances.

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICENewPackets.

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

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Événement NewInAirPackets**](inkpicture-newinairpackets.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




