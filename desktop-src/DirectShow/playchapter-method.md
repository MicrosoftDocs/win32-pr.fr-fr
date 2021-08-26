---
description: La méthode PlayChapter démarre la lecture à partir du chapitre spécifié dans le titre actuel.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Méthode PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102339"
---
# <a name="playchapter-method"></a>Méthode PlayChapter

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayChapter` méthode démarre la lecture à partir du chapitre spécifié dans le titre actuel.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Spécifie l’index de chapitre dans le titre actuel sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Quand la fin du chapitre spécifié est atteinte, cette méthode continue de visionner les chapitres suivants, le cas échéant. Si vous souhaitez lire uniquement un chapitre spécifié, utilisez [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



