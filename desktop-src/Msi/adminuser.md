---
description: Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propriété AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b765aa4ece1bc19b5ed59e97a98ca4579042d52d65c0024ae018c794f9aaa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581909"
---
# <a name="adminuser-property"></a>Propriété AdminUser

Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur.

**Windows Server 2008 et Windows Vista :** La propriété **adminuser** est la même que la propriété [**Privileged**](privileged.md) . Les auteurs doivent utiliser la propriété **Privileged** . Le programme d’installation définit ces propriétés si l’utilisateur dispose de privilèges d’administrateur, si l’application a été affectée par un administrateur système, ou si les stratégies d’utilisateur et d’ordinateur AlwaysInstallElevated a sont définies sur true.

## <a name="remarks"></a>Remarques

Les différences entre ces propriétés peuvent avoir été utilisées dans certains packages hérités. Par exemple, **adminuser** peut avoir été utilisé à la place de [**Privileged**](privileged.md) dans des instructions conditionnelles, car le programme d’installation définit uniquement la propriété **adminuser** si l’utilisateur est un administrateur. Le programme d’installation définit la propriété **Privileged** si l’utilisateur est un administrateur ou si la stratégie permet à l’utilisateur d’installer avec des privilèges élevés.

**Windows Server 2008 et Windows Vista :** Non pris en charge. Les [**privilèges**](privileged.md) et les **adminuser** sont les mêmes. Les packages qui requièrent des propriétés distinctes **privilégiées** et **adminuser** peuvent restaurer la différence en définissant la propriété [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .

Pour plus d’informations, consultez [installation d’un package avec des privilèges élevés pour une propriété non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)et [**privilégié**](privileged.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Vista ou Windows Server 2008. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




