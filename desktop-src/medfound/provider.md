---
description: Spécifie un fournisseur de trace (ETW ou WPP) pour MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (élément)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4213e4d56f8dc2ed73802650e3c7558736cedea8f69fe2148b638fbb92433474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034967"
---
# <a name="provider-element"></a>provider (élément)

Spécifie un fournisseur de trace (ETW ou WPP) pour [MFTrace](mftrace.md).

## <a name="usage"></a>Usage

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Attributs



| Attribut            | Type             | Obligatoire       | Description                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **Identifiant**<br/>    | CDATA<br/> | Oui<br/> | Nom ou GUID du fournisseur.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Oui<br/> | Niveau de trace.<br/> <br/>                  |



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

 

 




