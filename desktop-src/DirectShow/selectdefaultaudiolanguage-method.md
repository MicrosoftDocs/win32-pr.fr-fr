---
description: La méthode SelectDefaultAudioLanguage définit la langue audio par défaut actuelle dans l’objet MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Méthode SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521276"
---
# <a name="selectdefaultaudiolanguage-method"></a>Méthode SelectDefaultAudioLanguage

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SelectDefaultAudioLanguage` méthode définit la langue audio par défaut actuelle dans l’objet mswebdvd.

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Spécifie la langue sous la forme d’une valeur LCID entière.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Spécifie l’extension de langage audio DVD en tant que valeur entière.



| Valeur | Description       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Sous-titres          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



