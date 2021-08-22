---
description: La propriété ComponentPath est une propriété en lecture seule qui retourne le chemin d’accès complet à un composant installé. Si le chemin d’accès à la clé du composant est une clé de Registre, la clé de Registre est retournée.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer. ComponentPath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 88601dc4c65d0d3f69a5386ed62d1523c9fa21723e73b1ad4d208d0eff437658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632622"
---
# <a name="installercomponentpath-property"></a>Installer. ComponentPath, propriété

La propriété **ComponentPath** est une propriété en lecture seule qui retourne le chemin d’accès complet à un composant installé. Si le chemin d’accès à la clé du composant est une clé de Registre, la clé de Registre est retournée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Si le composant est une clé de Registre, les racines du Registre sont représentées par ordre numérique. Par exemple, le chemin d’accès au registre « HKEY \_ Current \_ User \\ Software \\ Microsoft » est retourné sous la forme « 01 : \\ Software \\ Microsoft ». Les racines de Registre retournées sont définies comme suit :



| Root                    | Valeur renvoyée |
|-------------------------|----------------|
| \_racine des classes HKEY \_     | 00             |
| HKEY \_ Current \_ User     | 01             |
| HKEY \_ local \_ machine    | 02             |
| HKEY, \_ utilisateurs             | 03             |
| \_données de performances HKEY \_ | 04             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




