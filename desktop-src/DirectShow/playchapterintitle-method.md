---
description: La méthode PlayChapterInTitle lit le chapitre spécifié dans le titre spécifié.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Méthode PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007467"
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

## <a name="remarks"></a>Notes

Cette méthode démarre la lecture au chapitre spécifié, puis continue la lecture indéfiniment. Si vous souhaitez lire uniquement un chapitre particulier, utilisez [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

 

 



