---
description: Supprime une source réseau ou URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Méthode patch. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123646"
---
# <a name="patchsourcelistclearsource-method"></a>Méthode patch. SourceListClearSource

La méthode **SourceListClearSource** supprime une source réseau ou URL. Cette méthode appelle [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* 
</dt> <dd>

Type de source à supprimer.

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

**\_réseau MSISOURCETYPE**
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

**\_URL MSISOURCETYPE**
</dt> </dl> </dd> <dt>

*SourcePath* 
</dt> <dd>

Chemin d’accès à la source à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




