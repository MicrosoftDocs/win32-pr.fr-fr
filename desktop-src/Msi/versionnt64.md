---
description: Le programme d’installation définit la propriété VersionNT64 sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriété VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285f97a6325df65ace9ff6620489697e6eeeb573761437bd0a826dec4dc31e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526929"
---
# <a name="versionnt64-property"></a>Propriété VersionNT64

Le programme d’installation définit la propriété **VersionNT64** sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits. La propriété n’est pas définie si le système d’exploitation n’est pas 64 bits.

La valeur est un entier : MajorVersion \* 100 + MinorVersion.

pour des raisons de compatibilité, la propriété est également non définie si la propriété [**résumé du modèle**](template-summary.md) indique que le package est destiné aux systèmes intel (x86) 32 bits et que le système d’exploitation ne peut pas exécuter le code intel (x64) 64 bits, par exemple Windows 10 sur ARM (ARM64).

> [!NOTE]
> à partir de Windows 10 build 21277, ARM64 est généré dans le canal de développement du programme Windows Insider Preview prend en charge les applications x64. Sur ces builds ARM64, la propriété VersionNT64 est définie pour les packages x86.

## <a name="remarks"></a>Remarques

les expressions conditionnelles testent l’utilisation de 64 bits Windows simplement en utilisant le nom de la propriété ou en vérifiant la version à l’aide d’un opérateur de comparaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows le programme d’installation sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Windows Service Pack minimale requise par une version Windows Installer, consultez la [configuration requise](windows-installer-portal.md) pour la Run-Time de Windows Installer.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




