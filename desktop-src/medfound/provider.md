---
description: Spécifie un fournisseur de trace (ETW ou WPP) pour MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (élément)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118444"
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
| [**éditeurs**](providers.md)<br/> |



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

 

 




