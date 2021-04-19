---
description: Le programme d’installation définit la propriété UILevel sur le niveau de l’interface utilisateur.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propriété UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539659"
---
# <a name="uilevel-property"></a>Propriété UILevel

Le programme d’installation définit la propriété **UILevel** sur le niveau de l’interface utilisateur. L’interface utilisateur interne est activée et définie par [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Cette propriété est définie sur l’un des types de données INSTALLUILEVEL suivants.



| INSTALLUILEVEL          | Valeur numérique | Niveau de l’interface utilisateur                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ aucun    | 2             | Installation entièrement sans assistance :             |
| INSTALLUILEVEL de \_ base   | 3             | Progression et gestion des erreurs simples.         |
| INSTALLUILEVEL \_ réduit | 4             | Interface utilisateur créée, boîtes de dialogue d’Assistant supprimées.     |
| INSTALLUILEVEL \_ Full    | 5             | Interface utilisateur créée avec les assistants, la progression, les erreurs. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Interface utilisateur](user-interface.md)
</dt> <dt>

[Détermination du niveau d’interface utilisateur à partir d’une action personnalisée](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




