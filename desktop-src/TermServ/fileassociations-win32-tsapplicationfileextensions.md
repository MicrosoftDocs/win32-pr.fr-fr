---
title: Méthode FileAssociations de la classe Win32_TSApplicationFileExtensions
description: Analyse le registre pour obtenir les associations de fichiers actuelles pour une application.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FileAssociations
- Services Bureau à distance de la méthode FileAssociations, classe Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance, méthode FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536921"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Méthode FileAssociations de la \_ classe Win32 TSApplicationFileExtensions

Analyse le registre pour obtenir les associations de fichiers actuelles pour une application.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin* \[ dans\]
</dt> <dd>

Spécifie le chemin d’accès à l’application.

</dd> <dt>

*FileAssociations* \[ à\]
</dt> <dd>

En cas de réussite, contient les associations de fichiers pour cette application.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**\_RDFileAssociation Win32**](win32-rdfileassociation.md)
</dt> </dl>

 

 





