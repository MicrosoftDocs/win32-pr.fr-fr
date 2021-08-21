---
description: 'la propriété Version9X fournit le numéro de version des versions 9x de Windows systèmes d’exploitation. La valeur de cette propriété est un entier : MajorVersion \* 100 + MinorVersion.'
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Propriété Version9X
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbf76faef4ead06043e4824b6b8f0989a64e261b7c48e260c9c25fa58381cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498999"
---
# <a name="version9x-property"></a>Propriété Version9X

la propriété **Version9X** fournit le numéro de version des versions 9x de Windows systèmes d’exploitation.

La valeur de cette propriété est un entier : MajorVersion \* 100 + MinorVersion. La propriété reste non définie si le système d’exploitation n’est pas une version 9x. Pour plus d’informations, consultez [valeurs de propriété du système d’exploitation](operating-system-property-values.md).

## <a name="remarks"></a>Remarques

Les expressions de condition peuvent tester la version à l’aide du nom de propriété ou peuvent vérifier la version à l’aide d’un opérateur de comparaison.

Tous les noms de propriété respectent la casse. Notez que le X dans le nom **Version9X** est en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




