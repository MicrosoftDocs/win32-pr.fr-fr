---
description: Affectez à la propriété MSIUSEREALADMINDETECTION la valeur 1 pour demander que le programme d’installation utilise les informations utilisateur réelles lors de la définition de la propriété AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propriété MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544475"
---
# <a name="msiuserealadmindetection-property"></a>Propriété MSIUSEREALADMINDETECTION

Affectez à la propriété **MSIUSEREALADMINDETECTION** la valeur 1 pour demander que le programme d’installation utilise les informations utilisateur réelles lors de la définition de la propriété [**adminuser**](adminuser.md) . En cas d’exécution sur Windows Vista, les [**privilèges**](privileged.md) et les **adminuser** sont les mêmes. Les auteurs doivent utiliser la propriété **Privileged** dans de nouveaux packages. Les packages hérités qui requièrent des propriétés distinct **Privileged** et **adminuser** peuvent restaurer la différence en définissant la propriété **MSIUSEREALADMINDETECTION** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




