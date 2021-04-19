---
description: La méthode Render Initialise le graphique de filtre DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Méthode Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544544"
---
# <a name="render-method"></a>Méthode Render

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Render` méthode initialise le graphique de filtre de DVD.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

Spécifie une valeur entière indiquant si le graphique de filtre sera détruit et reconstruit.



| Valeur | Description                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | Le graphique de filtre ne sera pas détruit et reconstruit s’il existe déjà. Il s’agit de la valeur par défaut. |
| 1     | Le graphique de filtre sera détruit et reconstruit s’il existe déjà.                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La `Render` méthode permet à l’objet **mswebdvd** d’initialiser complètement le graphique de filtre DirectShow sous-jacent au démarrage. Cela élimine le léger délai qui, autrement, se produit lorsque l’utilisateur émet la première commande pour lire un disque ou afficher un menu. Il n’existe aucun cas dans lequel `Render` doit être appelé avant d’appeler une autre méthode. Par exemple, si l’application appelle [**PlayTitle**](playtitle-method.md) avant que le graphique de filtre n’ait été initialisé, l’objet **mswebdvd** appelle `Render` automatiquement avant de tenter de lire le disque.

 

 



