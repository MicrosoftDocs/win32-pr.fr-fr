---
description: La méthode GetSubpictureLanguage récupère la langue du flux de sous-image spécifié.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Méthode GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536929"
---
# <a name="getsubpicturelanguage-method"></a>Méthode GetSubpictureLanguage

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetSubpictureLanguage` méthode récupère la langue du flux de sous-image spécifié.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le numéro de flux de sous-image dont vous souhaitez récupérer la langue de texte sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une chaîne explicite identifiant la langue du flux audio dans le titre actuel.

 

 



