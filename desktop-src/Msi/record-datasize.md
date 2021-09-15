---
description: La propriété DataSize de l’objet record est une propriété en lecture seule qui retourne la taille des données pour le champ désigné.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record. DataSize, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312266"
---
# <a name="recorddatasize-property"></a>Record. DataSize, propriété

La propriété **DataSize** de l’objet [**Record**](record-object.md) est une propriété en lecture seule qui retourne la taille des données pour le champ désigné. Si les données sont un flux, la longueur du flux en octets est retournée. Si les données sont une chaîne, la longueur de la chaîne sans valeur null est retournée. Si les données sont un entier, la valeur 4 est retournée (indiquant la taille de l’entier). Si les données ont la valeur null, la valeur 0 est retournée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




