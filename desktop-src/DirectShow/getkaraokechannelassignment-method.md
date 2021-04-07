---
description: La méthode GetKaraokeChannelAssignment récupère une valeur qui indique comment les canaux karaoké sont affectés aux intervenants.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Méthode GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846877"
---
# <a name="getkaraokechannelassignment-method"></a>Méthode GetKaraokeChannelAssignment

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetKaraokeChannelAssignment` méthode récupère une valeur qui indique comment les canaux karaoké sont affectés aux intervenants.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le flux audio sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier indiquant l’assignation de l’intervenant pour le flux spécifié.



| Code de retour | Description                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Le flux est affecté aux haut-parleurs gauche et droit.                  |
| 3           | Le flux est affecté aux haut-parleurs gauche, droit et moyen.         |
| 4           | Le flux est affecté aux haut-parleurs gauche, droite et Audio1.         |
| 5           | Le flux est affecté aux haut-parleurs gauche, droit, moyen et Audio1. |
| 6           | Le flux est affecté aux haut-parleurs gauche, droite et Audio2.         |
| 7           | Le flux est affecté aux haut-parleurs gauche, droit, moyen et Audio2. |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



