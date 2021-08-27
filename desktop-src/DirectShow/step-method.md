---
description: La méthode STEP avance le DVD-Video flux du nombre spécifié de frames.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5738e8704b24d64a429d8d38f1b9eac2f9b8ff7e22a7e9d1d2a29fb9df4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050309"
---
# <a name="step-method"></a>Step, méthode

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

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

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, appelez [**CanStep**](canstep-method.md) pour déterminer si le décodeur prend en charge l’exécution pas à pas.

Si le DVD-Video est lu en mode inverse lorsque cette méthode est appelée et que le décodeur prend en charge l’exécution pas à pas de l’image inverse, l’exécution pas à pas est effectuée en sens inverse.

 

 



