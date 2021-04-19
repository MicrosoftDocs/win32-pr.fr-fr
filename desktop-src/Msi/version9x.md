---
description: 'La propriété Version9X indique le numéro de version des versions 9x des systèmes d’exploitation Windows. La valeur de cette propriété est un entier : MajorVersion \* 100 + MinorVersion.'
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Propriété Version9X
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df599629fdf978837a8f53df7d1faa4f476db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528405"
---
# <a name="version9x-property"></a>Propriété Version9X

La propriété **Version9X** indique le numéro de version des versions 9x des systèmes d’exploitation Windows.

La valeur de cette propriété est un entier : MajorVersion \* 100 + MinorVersion. La propriété reste non définie si le système d’exploitation n’est pas une version 9x. Pour plus d’informations, consultez [valeurs de propriété du système d’exploitation](operating-system-property-values.md).

## <a name="remarks"></a>Notes

Les expressions de condition peuvent tester la version à l’aide du nom de propriété ou peuvent vérifier la version à l’aide d’un opérateur de comparaison.

Tous les noms de propriété respectent la casse. Notez que le X dans le nom **Version9X** est en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




