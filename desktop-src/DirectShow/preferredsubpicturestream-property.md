---
description: La propriété PreferredSubpictureStream récupère le flux de sous-image préféré pour la session d’affichage en cours.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propriété PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28b98163607e31a207bffb3974fee3b32505ff60ba3700b452b2dff2625f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583539"
---
# <a name="preferredsubpicturestream-property"></a>Propriété PreferredSubpictureStream

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PreferredSubpictureStream` propriété récupère le flux de sous-image préféré pour la session d’affichage en cours.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le flux de sous-image préféré actuel dans le registre système.

## <a name="remarks"></a>Remarques

Le flux de sous-image par défaut est défini avec [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)de l’objet [MSDVDAdm](msdvdadm-object.md) .

 

 



