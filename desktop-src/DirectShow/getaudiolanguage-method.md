---
description: La méthode GetAudioLanguage récupère une chaîne indiquant la langue disponible dans le flux audio spécifié.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Méthode GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007543"
---
# <a name="getaudiolanguage-method"></a>Méthode GetAudioLanguage

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetAudioLanguage` méthode récupère une chaîne indiquant la langue disponible dans le flux audio spécifié.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le numéro de flux audio dans le titre actuel sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une chaîne explicite identifiant la langue du flux audio dans le titre actuel.

 

 



