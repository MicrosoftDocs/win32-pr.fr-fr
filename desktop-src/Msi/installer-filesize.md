---
description: La méthode FileSize de l’objet installer utilise des appels d’API Win32 pour retourner la taille du fichier spécifié dans chemin d’accès.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. FileSize, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f585da776d348e7c774d4671a230881f2ec0e4ddaca8a63842d59a9b77a61972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630688"
---
# <a name="installerfilesize-method"></a>Installer. FileSize, méthode

La méthode **FileSize** de l’objet [**installer**](installer-object.md) utilise des appels d’API Win32 pour retourner la taille du fichier spécifié dans *chemin d’accès*.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Chaîne obligatoire contenant le chemin d’accès au fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




