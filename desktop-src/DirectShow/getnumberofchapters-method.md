---
description: La méthode GetNumberOfChapters récupère le nombre de chapitres dans le titre spécifié.
ms.assetid: d1291f6d-9296-486f-adad-d8819a4e54d6
title: Méthode GetNumberOfChapters
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c8774271cc66171b3f518d422ae2c3b46f1e278f2be29b481f0d2d683aa93f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756819"
---
# <a name="getnumberofchapters-method"></a>Méthode GetNumberOfChapters

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetNumberOfChapters` méthode récupère le nombre de chapitres dans le titre spécifié.

``` syntax
[iChapters = ] MSWebDVD.GetNumberOfChapters(iTitle)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie le titre sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière comprise entre 1 et 999 indiquant le nombre de chapitres.

 

 



