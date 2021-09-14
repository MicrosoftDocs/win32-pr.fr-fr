---
description: Contient une liste de fournisseurs de suivi pour MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers (élément)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235901"
---
# <a name="providers-element"></a>providers (élément)

Contient une liste de fournisseurs de suivi pour [MFTrace](mftrace.md).

## <a name="usage"></a>Usage

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | Spécifie le fournisseur de détournements de Media Foundation, qui effectue le suivi des appels d’API Media Foundation.<br/> <br/> |
| [**moteur**](provider.md)<br/>   | Spécifie un fournisseur de trace (ETW ou WPP).<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Éléments parents

Il n’y a pas d’éléments parents.

## <a name="element-information"></a>Informations sur les éléments

:::row:::
    :::column:::
        Peut être vide
    :::column-end:::
    :::column span="2":::
        Oui
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




