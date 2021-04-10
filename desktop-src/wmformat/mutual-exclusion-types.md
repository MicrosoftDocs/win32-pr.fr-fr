---
title: Types d’exclusion mutuelle
description: Types d’exclusion mutuelle
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK, exclusion mutuelle
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- exclusion mutuelle, types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030764"
---
# <a name="mutual-exclusion-types"></a>Types d’exclusion mutuelle

Vous pouvez utiliser des types d’exclusion mutuelle pour identifier la nature d’un objet d’exclusion mutuelle dans un profil. Les types d’exclusion mutuelle sont utilisés comme paramètres pour [**IWMMutualExclusion :: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) et [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).

Le tableau suivant répertorie les identificateurs pour les types d’exclusion mutuelle.



| Constante de type d’exclusion mutuelle | GUID                                 |
|--------------------------------|--------------------------------------|
| \_Langue WMMUTEX \_ CLSID       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| \_Débit binaire WMMUTEX du CLSID \_        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| Présentation du CLSID \_ WMMUTEX \_   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ inconnu        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Valeurs GUID**](guid-values.md)
</dt> </dl>

 

 




