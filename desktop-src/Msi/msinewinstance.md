---
description: La propriété MSINEWINSTANCE indique l’installation d’une nouvelle instance d’un produit avec des transformations d’instance.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propriété MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b26831f1171813d9df9e2c4124a4d6c24ea7efbf707fc5c15eefc9d6a8b1046
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082849"
---
# <a name="msinewinstance-property"></a>Propriété MSINEWINSTANCE

La propriété **MSINEWINSTANCE** indique l’installation d’une nouvelle instance d’un produit avec des transformations d’instance. Cette propriété prend en charge plusieurs instances par le biais du code de produit – modification des transformations. La valeur de cette propriété est 1. La présence de cette propriété sur la ligne de commande nécessite que la propriété [**TRANSformations**](transforms.md) soit également présente. La première transformation figurant dans **TRANSformations** doit être une transformation d’instance. Pour plus d’informations, consultez [installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md)

cette propriété est disponible avec le programme d’installation qui exécute un système dans le Windows Server 2003 ou Windows XP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




