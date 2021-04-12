---
description: La méthode PlayChaptersAutoStop démarre la lecture au chapitre spécifié dans le titre spécifié et pour le nombre de chapitres spécifié.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Méthode PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200724"
---
# <a name="playchaptersautostop-method"></a>Méthode PlayChaptersAutoStop

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayChaptersAutoStop` méthode démarre la lecture au chapitre spécifié dans le titre spécifié et pour le nombre de chapitres spécifié.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie le titre sous la forme d’une valeur entière.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Spécifie le chapitre de démarrage sous la forme d’une valeur entière.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Spécifie le nombre de chapitres à lire sous la forme d’une valeur entière.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Lorsque le dernier chapitre a joué, cette méthode entraîne l’envoi à l’application d’une notification d’événement [**\_ \_ \_ autostop du chapitre de DVD ce**](ec-dvd-chapter-autostop.md) .

 

 



