---
description: Le programme d’installation définit la propriété VersionNT64 sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriété VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526043"
---
# <a name="versionnt64-property"></a>Propriété VersionNT64

Le programme d’installation définit la propriété **VersionNT64** sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits. La propriété n’est pas définie si le système d’exploitation n’est pas 64 bits.

La valeur est un entier : MajorVersion \* 100 + MinorVersion.

Pour des raisons de compatibilité, la propriété est également non définie si la propriété [**Résumé du modèle**](template-summary.md) indique que le package est destiné aux systèmes Intel 32 bits et que le système d’exploitation est une architecture 64 bits qui n’est pas Intel64 ou x64 (comme ARM64).

## <a name="remarks"></a>Notes

Les expressions conditionnelles testent les fenêtres 64 bits simplement en utilisant le nom de la propriété ou en vérifiant la version à l’aide d’un opérateur de comparaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




