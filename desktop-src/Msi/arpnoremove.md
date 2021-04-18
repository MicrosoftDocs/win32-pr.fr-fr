---
description: La définition de la propriété ARPNOREMOVE désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui supprime le produit.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propriété ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540275"
---
# <a name="arpnoremove-property"></a>Propriété ARPNOREMOVE

La définition de la propriété **ARPNOREMOVE** désactive la fonctionnalité **Ajout/suppression de programmes** du panneau de **configuration** qui supprime le produit. Pour Windows 2000, le bouton **supprimer** du produit est désactivé à partir de l’option **Ajout/suppression de programmes** du **panneau de configuration**. Pour les systèmes d’exploitation antérieurs, cela a pour effet de supprimer le produit de la liste des produits installés dans le panneau de **configuration** **Ajout/suppression de programmes** .

Si la propriété **ARPNOREMOVE** est définie, l' [action RegisterProduct](registerproduct-action.md) écrit la valeur « NoRemove » sous la clé de Registre :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **{*clé de produit*}**

La définition de la propriété **ARPNOREMOVE** empêche l’écriture de la valeur UninstallString sous cette clé. La valeur UnistallString est une ligne de commande pour la suppression du produit, au lieu de la reconfiguration du produit.

## <a name="remarks"></a>Notes

Par exemple, cette propriété peut être définie au cours d’une transformation de personnalisation pour empêcher les utilisateurs de supprimer une personnalisation d’administrateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 ou version ultérieure sur Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




