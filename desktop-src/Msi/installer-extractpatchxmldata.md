---
description: La méthode ExtractPatchXMLData de l’objet installer extrait des informations d’un correctif sous forme de chaîne XML. Les informations peuvent être utilisées pour déterminer si le correctif s’applique sur un système cible. Cette méthode appelle MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer. ExtractPatchXMLData, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525947"
---
# <a name="installerextractpatchxmldata-method"></a>Installer. ExtractPatchXMLData, méthode

La méthode **ExtractPatchXMLData** de l’objet [**installer**](installer-object.md) extrait des informations d’un correctif sous forme de chaîne XML. Les informations peuvent être utilisées pour déterminer si le correctif s’applique sur un système cible. Cette méthode appelle [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PatchPath* 
</dt> <dd>

Chemin d’accès complet au correctif à partir duquel les informations de mise en application doivent être extraites.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




