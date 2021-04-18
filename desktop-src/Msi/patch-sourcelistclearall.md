---
description: La méthode SourceListClearAll de l’objet patch efface la liste source complète de toutes les sources du type spécifié pour un correctif. Accepte le type en tant que paramètre. Cette méthode appelle MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Méthode patch. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540536"
---
# <a name="patchsourcelistclearall-method"></a>Méthode patch. SourceListClearAll

La méthode **SourceListClearAll** de l’objet [**patch**](patch-object.md) efface la liste source complète de toutes les sources du type spécifié pour un correctif. Accepte le *type* en tant que paramètre. Cette méthode appelle [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* 
</dt> <dd>

Type de source, par exemple, réseau, URL ou média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




