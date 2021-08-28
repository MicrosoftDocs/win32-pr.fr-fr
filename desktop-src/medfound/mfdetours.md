---
description: Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: élément mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113639"
---
# <a name="mfdetours-element"></a>élément mfdetours

Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.

## <a name="usage"></a>Usage

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Attributs



| Attribut            | Type             | Obligatoire       | Description                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Oui<br/> | Niveau de trace.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                               |
|---------------------------------------|
| [**mot**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
keyword+
```

## <a name="parent-elements"></a>Éléments parents

| Élément                                   |
|-------------------------------------------|
| [**fournisseurs**](providers.md)<br/> |



## <a name="element-information"></a>Informations sur les éléments

:::row:::
    :::column:::
        Peut être vide
    :::column-end:::
    :::column span="2":::
        Non
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




