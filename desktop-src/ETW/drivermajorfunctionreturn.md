---
description: Cette classe est la classe de type d’événement pour les événements de retour d’appel de fonction principale du pilote. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: DriverMajorFunctionReturn, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: de8c18d7655aec0f9ae4748c384b26015a5a1083721aae367e132ea7c39f80a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914469"
---
# <a name="drivermajorfunctionreturn-class"></a>DriverMajorFunctionReturn, classe

Cette classe est la classe de type d’événement pour les événements de retour d’appel de fonction principale du pilote.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membres

La classe **DriverMajorFunctionReturn** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **DriverMajorFunctionReturn** possède les propriétés suivantes.

<dl> <dt>

**Paquets**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Paquet de demande d’e/s.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Identificateur qui identifie de façon unique la demande. Utilisez cet identificateur pour établir une corrélation avec les autres événements de pilote, par exemple l’événement [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**E**](diskio.md)
</dt> </dl>

 

 




