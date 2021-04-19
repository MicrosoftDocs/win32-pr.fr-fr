---
description: La méthode CreateRecord de l’objet installer retourne un nouvel objet enregistrement avec le nombre demandé de champs.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. CreateRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528843"
---
# <a name="installercreaterecord-method"></a>Installer. CreateRecord, méthode

La méthode **CreateRecord** de l’objet [**installer**](installer-object.md) retourne un nouvel objet [**enregistrement**](record-object.md) avec le nombre demandé de champs.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*count* 
</dt> <dd>

Nombre de champs requis, qui peut être égal à 0. Le nombre maximal de champs dans un enregistrement est limité à 65535.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le champ 0, et non l’un des champs dans *Count*, est normalement utilisé pour les éléments orientés enregistrement, tels que les chaînes de format ou les codes d’exécution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




