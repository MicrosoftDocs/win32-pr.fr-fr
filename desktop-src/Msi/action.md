---
description: La propriété ACTION peut être définie sur les valeurs suivantes.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092897"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




