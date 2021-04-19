---
description: La méthode SetStream de l’objet record copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux. Les données de flux ne peuvent pas être insérées dans les champs temporaires.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Record. SetStream, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521654"
---
# <a name="recordsetstream-method"></a>Record. SetStream, méthode

La méthode **SetStream** de l’objet [**Record**](record-object.md) copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux. Les données de flux ne peuvent pas être insérées dans les champs temporaires.

## <a name="syntax"></a>Syntaxe


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*case* 
</dt> <dd>

Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.

</dd> <dt>

*cheminfichier* 
</dt> <dd>

Emplacement du fichier à copier. Aucune traduction de tout type n’est effectuée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




