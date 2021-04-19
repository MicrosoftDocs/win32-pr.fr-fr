---
description: La propriété DefaultUIFont définit le style de police par défaut utilisé pour les contrôles. Pour spécifier la valeur par défaut, définissez DefaultUIFont sur l’un des styles prédéfinis dans la table TextStyle de la table Property.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propriété DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541558"
---
# <a name="defaultuifont-property"></a>Propriété DefaultUIFont

La propriété **DefaultUIFont** définit le style de police par défaut utilisé pour les contrôles. Pour spécifier la valeur par défaut, définissez **DefaultUIFont** sur l’un des styles prédéfinis dans la [table TextStyle](textstyle-table.md) de la [table Property](property-table.md).

## <a name="remarks"></a>Notes

La propriété **DefaultUIFont** de chaque package d’installation avec une interface utilisateur doit être définie dans la [table de propriétés](property-table.md) avec l’un des styles prédéfinis listés dans le [tableau TextStyle](textstyle-table.md). Si cette propriété n’est pas spécifiée, le programme d’installation utilise la police système. Ainsi, le programme d’installation peut afficher de manière incorrecte les chaînes de texte lorsque la page de codes du package est différente de la page de codes de l’interface utilisateur par défaut de l’utilisateur.

Le texte et le style de police d’un contrôle peuvent être définis comme décrit dans [Ajout de contrôles et de texte](adding-controls-and-text.md). Si la chaîne de caractères figurant dans la colonne text de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md) ne spécifie pas le style de police, le contrôle utilise la valeur de la propriété **DefaultUIFont** comme style de police.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




