---
title: Élément LOGURL
description: L’élément LOGURL indique au lecteur Windows Media de soumettre toutes les données de journal à l’URL spécifiée.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Élément LOGURL lecteur Windows Media
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526072"
---
# <a name="logurl-element"></a>Élément LOGURL

L’élément **LOGURL** indique au lecteur Windows Media de soumettre toutes les données de journal à l’URL spécifiée.

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un hôte capable de traiter les demandes de journalisation.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

L’élément **LOGURL** permet à une sélection de métafichier client d’envoyer des informations de journalisation supplémentaires à des serveurs spécifiés. Les informations de journalisation sont automatiquement envoyées au serveur d’origine d’une sélection quand elle est ouverte et à chaque **LOGURL** spécifié pour l’élément **ASX** , le cas échéant. Les informations de journalisation sont également envoyées à chaque **LOGURL** spécifié pour un élément d' **entrée** lorsque cette entrée est atteinte. L’URL spécifiée dans l’attribut **href** d’un élément **LOGURL** doit être l’adresse d’un hôte qui est en mesure de traiter les demandes de journalisation. L’URL peut être n’importe quelle URL HTTP valide. L’URL peut également indiquer l’emplacement d’un script CGI.

Les seuls protocoles valides pour un élément **LOGURL** sont HTTP et HTTPS.

Un élément **LOGURL** dans la portée d’un élément **ASX** est uniquement applicable au métafichier dans lequel il réside, que ce métafichier soit référencé ou non à partir d’un autre métafichier. Un élément **LOGURL** force l’envoi de données de journal pour tout le contenu diffusé en continu à partir de son étendue définie et uniquement pour le contenu diffusé en continu à partir de son étendue définie. Les données de journal sont envoyées au serveur d’origine et à toutes les URL listées dans chaque élément **LOGURL** de l’étendue. Les données de journal ne sont envoyées qu’une seule fois à chaque URL de la liste, même si la même URL est listée plusieurs fois dans une étendue donnée. La répétition d’une **entrée** entraînerait une autre soumission aux URL listées.

Il n’existe aucune limite quant au nombre d’éléments **LOGURL** dans une sélection de métafichiers.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



Voici des exemples d’URL valides.

URL d’une application ISAPI :


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



URL d’un script CGI :


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



Une URL HTTP valide :


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





