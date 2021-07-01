---
description: Spécifie un mot clé pour un fournisseur MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Keyword, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119374"
---
# <a name="keyword-element"></a>Keyword, élément

Spécifie un mot clé pour un fournisseur [MFTrace](mftrace.md) .

## <a name="usage"></a>Usage

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Attributs



| Attribut         | Type             | Obligatoire       | Description                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **Identifiant**<br/> | CDATA<br/> | Oui<br/> | Nom ou masque du mot clé<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents

| Élément                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**moteur**](provider.md)<br/>   |



## <a name="remarks"></a>Remarques

Pour l’élément [**mfdetours**](mfdetours.md) , les mots clés valides sont répertoriés dans la rubrique [MFTrace Keywords](mftrace-keywords.md).

Pour l’élément [**Provider**](provider.md) , les mots clés dépendent du fournisseur d’événements. Vous pouvez utiliser l’utilitaire Wevtutil.exe pour répertorier les mots clés d’un fournisseur donné.

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
</dt> <dt>

[Mots clés MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 




