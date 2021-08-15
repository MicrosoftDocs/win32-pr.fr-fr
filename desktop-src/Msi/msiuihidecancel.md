---
description: cette propriété de Windows Installer indique que le niveau de l’interface utilisateur interne a été défini pour masquer le bouton annuler.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propriété MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da3c0888ea760e7e8627710b061112d350f94af569697b7ad0616d1dbacbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943987"
---
# <a name="msiuihidecancel-property"></a>Propriété MsiUIHideCancel

Le programme d’installation définit la propriété **MsiUIHideCancel** sur 1 lorsque le niveau de l’interface utilisateur interne a été défini pour inclure INSTALLUILEVEL \_ HIDECANCEL avec la fonction [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ou la propriété [UILevel](installer-uilevel.md)de l’objet [**installer**](installer-object.md) ou à l’aide des options de [ligne de commande](command-line-options.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




