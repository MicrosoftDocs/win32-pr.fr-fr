---
description: La méthode PlayChapterInTitle lit le chapitre spécifié dans le titre spécifié.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Méthode PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830869"
---
# <a name="playchapterintitle-method"></a>Méthode PlayChapterInTitle

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayChapterInTitle` méthode lit le chapitre spécifié dans le titre spécifié.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie le titre sous la forme d’une valeur entière.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Spécifie le chapitre sous la forme d’une valeur entière.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Cette méthode démarre la lecture au chapitre spécifié, puis continue la lecture indéfiniment. Si vous souhaitez lire uniquement un chapitre particulier, utilisez [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

 

 



