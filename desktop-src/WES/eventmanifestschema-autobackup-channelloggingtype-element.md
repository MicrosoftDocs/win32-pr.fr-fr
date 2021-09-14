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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852802"
---
# <a name="autobackup-channelloggingtype-element"></a>Élément de sauvegarde autoChannelLoggingType

Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

L’élément **Autobackup** est défini par le type complexe [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**journalisation (ChannelType)**](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





