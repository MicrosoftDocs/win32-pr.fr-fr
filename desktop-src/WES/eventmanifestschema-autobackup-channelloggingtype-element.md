---
title: Élément de sauvegarde autoChannelLoggingType
description: Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- EventLog, élément d’élément de sauvegarde
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519082"
---
# <a name="autobackup-channelloggingtype-element"></a>Élément de sauvegarde autoChannelLoggingType

Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

L’élément **Autobackup** est défini par le type complexe [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**journalisation (ChannelType)**](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





