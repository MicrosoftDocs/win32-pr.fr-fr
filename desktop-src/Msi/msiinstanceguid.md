---
description: La présence de la propriété MSIINSTANCEGUID indique qu’un code produit&\# 8211 ; la modification de la transformation est enregistrée dans le produit.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propriété MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543786"
---
# <a name="msiinstanceguid-property"></a>Propriété MSIINSTANCEGUID

La présence de la propriété **MSIINSTANCEGUID** indique qu’un code de produit-modification de la transformation est enregistré dans le produit. La valeur de la propriété **MSIINSTANCEGUID** spécifie l’instance d’un produit à utiliser pour l’installation. La propriété **MSIINSTANCEGUID** peut uniquement faire référence à un produit qui a déjà été installé avec une transformation d’instance.

Les transformations d’instance sont du code de produit : modification des transformations disponibles avec le programme d’installation qui s’exécute sur Windows Server 2003 ou Windows XP. Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




