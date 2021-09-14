---
title: Méthode GetIcon de la classe Win32_TSGetIcon
description: Retourne le contenu de l’icône spécifiée.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetIcon
- Services Bureau à distance de la méthode GetIcon, classe Win32_TSGetIcon
- Win32_TSGetIcon de la classe Services Bureau à distance, méthode GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920167"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Méthode GetIcon de la \_ classe Win32 TSGetIcon

Retourne le contenu de l’icône spécifiée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FilePath* \[ dans\]
</dt> <dd>

Spécifie le chemin d’accès au fichier qui contient l’icône

</dd> <dt>

*Index* \[ dans\]
</dt> <dd>

Spécifie l’index de l’icône dans le fichier.

</dd> <dt>

*IconContents* \[ à\]
</dt> <dd>

En cas de réussite, contient le contenu de l’icône.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGetIcon Win32**](win32-tsgeticon.md)
</dt> </dl>

 

 





