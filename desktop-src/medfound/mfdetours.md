---
description: Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: élément mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533768"
---
# <a name="mfdetours-element"></a>élément mfdetours

Spécifie le fournisseur de détournements de Microsoft Media Foundation, qui effectue le suivi des appels d’API Media Foundation.

## <a name="usage"></a>Utilisation

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
| [**keyword**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
keyword+
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                   |
|-------------------------------------------|
| [**fournisseurs**](providers.md)<br/> |



## <a name="element-information"></a>Informations sur les éléments



|              |     |
|--------------|-----|
| Peut être vide | Non  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




