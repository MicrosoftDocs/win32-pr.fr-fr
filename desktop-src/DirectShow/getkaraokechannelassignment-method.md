---
description: La méthode GetKaraokeChannelAssignment récupère une valeur qui indique comment les canaux karaoké sont affectés aux intervenants.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Méthode GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812549"
---
# <a name="getkaraokechannelassignment-method"></a>Méthode GetKaraokeChannelAssignment

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

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

 

 



