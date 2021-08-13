---
description: La méthode FileVersion de l’objet installer retourne la chaîne de version ou la chaîne de langue du chemin d’accès spécifié dans le chemin d’accès à l’aide du format dans lequel le programme d’installation s’attend à les trouver dans la base de données.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 492ebb0c7678b7819f3abc423517dcf77d071b81009c3b12017b1b627bb84057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630581"
---
# <a name="installerfileversion-method"></a>Installer. FileVersion, méthode

La méthode **FileVersion** de l’objet [**installer**](installer-object.md) retourne la chaîne de version ou la chaîne de langue du chemin d’accès spécifié dans le *chemin d’accès* à l’aide du format dans lequel le programme d’installation s’attend à les trouver dans la base de données. Pour les versions, il s’agit d’une chaîne au \# format « . \# . \# . \# ». Pour la langue, il s’agit de l’ID de langue décimale.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Chaîne obligatoire contenant le chemin d’accès au fichier.

</dd> <dt>

*Langage* 
</dt> <dd>

Indicateur de désignation indiquant si la valeur retournée est un ID de langue ou une chaîne de version. TRUE retourne la langue, FALSe retourne la version. Ce paramètre est facultatif, avec FALSe comme valeur par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




