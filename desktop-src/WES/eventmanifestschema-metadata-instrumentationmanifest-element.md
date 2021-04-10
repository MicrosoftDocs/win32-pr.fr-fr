---
title: Élément Metadata (instrumentationManifest)
description: Contient des valeurs globales que vous pouvez référencer dans d’autres manifestes.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog (élément de métadonnées)
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102932"
---
# <a name="metadata-instrumentationmanifest-element"></a>Élément Metadata (instrumentationManifest)

Contient des valeurs globales que vous pouvez référencer dans d’autres manifestes. Pour obtenir un exemple, consultez le fichier Winmeta.xml inclus dans le \\ dossier include du SDK Windows.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

L’élément **Metadata** est défini par l’élément [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Notes

Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





