---
description: Spécifie un fournisseur de trace (ETW ou WPP) pour MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (élément)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753900"
---
# <a name="provider-element"></a>provider (élément)

Spécifie un fournisseur de trace (ETW ou WPP) pour [MFTrace](mftrace.md).

## <a name="usage"></a>Utilisation

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

 

 




