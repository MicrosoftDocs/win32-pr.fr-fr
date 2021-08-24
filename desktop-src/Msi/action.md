---
description: La propriété ACTION peut être définie sur les valeurs suivantes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145992"
---
# <a name="action-property"></a>ACTION, propriété

La propriété **action** peut être définie sur les valeurs suivantes.

## <a name="value"></a>Valeur



| Valeur                                                                                                                                            | Signification                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**INSTALLER**</dt> </dl>       | [Action d’installation](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**PUBLIÉS**</dt> </dl> | [Action de publication](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ADMINISTRATEUR**</dt> </dl>             | [Action d’administration](admin-action.md)<br/>         |



 

La propriété **action** détermine l’action à effectuer si un nom d’action null est fourni à [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou à la [**méthode d’action**](session-doaction.md). Si aucune valeur n’est définie pour la propriété **action** , le programme d’installation appelle l' [action d’installation](install-action.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




