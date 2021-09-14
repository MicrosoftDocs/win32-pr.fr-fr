---
description: La propriété PreferredSubpictureStream récupère le flux de sous-image préféré pour la session d’affichage en cours.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propriété PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223172"
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

## <a name="remarks"></a>Notes

Le flux de sous-image par défaut est défini avec [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)de l’objet [MSDVDAdm](msdvdadm-object.md) .

 

 



