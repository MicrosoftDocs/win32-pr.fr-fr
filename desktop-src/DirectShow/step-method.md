---
description: La méthode STEP avance le DVD-Video flux du nombre spécifié de frames.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521900"
---
# <a name="step-method"></a>Step, méthode

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Step` méthode avance le DVD-Video flux du nombre spécifié de frames.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Spécifie le nombre de frames à exécuter pas à pas sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, appelez [**CanStep**](canstep-method.md) pour déterminer si le décodeur prend en charge l’exécution pas à pas.

Si le DVD-Video est lu en mode inverse lorsque cette méthode est appelée et que le décodeur prend en charge l’exécution pas à pas de l’image inverse, l’exécution pas à pas est effectuée en sens inverse.

 

 



