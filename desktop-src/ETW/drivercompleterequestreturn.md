---
description: Cette classe est la classe de type d’événement pour les événements de retour de demande de pilote complets. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: DriverCompleteRequestReturn, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224284"
---
# <a name="drivercompleterequestreturn-class"></a>DriverCompleteRequestReturn, classe

Cette classe est la classe de type d’événement pour les événements de retour de demande de pilote complets.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membres

La classe **DriverCompleteRequestReturn** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **DriverCompleteRequestReturn** possède les propriétés suivantes.

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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**E**](diskio.md)
</dt> </dl>

 

 




