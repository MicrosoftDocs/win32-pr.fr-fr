---
description: La méthode IsAudioStreamEnabled récupère une valeur indiquant si le flux audio spécifié est activé dans le titre actuel.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Méthode IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520396"
---
# <a name="isaudiostreamenabled-method"></a>Méthode IsAudioStreamEnabled

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `IsAudioStreamEnabled` méthode récupère une valeur indiquant si le flux audio spécifié est activé dans le titre actuel.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le flux audio sous la forme d’une valeur entière comprise entre 0 et 7.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si le flux audio spécifié est disponible pour le titre actuel. True signifie qu’il est disponible.

## <a name="remarks"></a>Notes

Bien qu’un disque puisse contenir jusqu’à huit flux audio indépendants, chaque flux n’est pas nécessairement disponible pour chaque titre. Par exemple, un titre de film principal peut avoir trois flux audio pour l’anglais, l’espagnol et le japonais, mais le titre « prochains attractions » peut avoir un seul flux audio en anglais. Vérifiez toujours qu’un flux est disponible pour un titre avant de définir la propriété [**CurrentAudioStream**](currentaudiostream-property.md) .

 

 



