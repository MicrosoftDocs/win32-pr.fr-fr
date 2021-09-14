---
description: La définition de la propriété ARPNOMODIFY désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui modifie le produit.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propriété ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092594"
---
# <a name="arpnomodify-property"></a>Propriété ARPNOMODIFY

La définition de la propriété **ARPNOMODIFY** désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui modifie le produit. pour Windows 2000, le bouton **modifier** du produit est désactivé dans **ajout/suppression de programmes** dans le **panneau de configuration**. Sur les systèmes d’exploitation antérieurs, le fait de cliquer sur le bouton **Ajout/suppression de programmes** désinstalle le produit plutôt que d’entrer dans l’Assistant mode de maintenance.

Si la propriété **ARPNOMODIFY** est définie, l' [action RegisterProduct](registerproduct-action.md) écrit la valeur « nomodify » sous la clé de Registre :

**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **{*clé de produit*}**

Si la propriété **ARPNOMODIFY** est définie et que la propriété [**ARPNOREMOVE**](arpnoremove.md) n’est pas définie, l’action RegisterProduct écrit également la valeur UninstallString sous cette clé. La valeur UnistallString est une ligne de commande pour la suppression du produit, au lieu de la reconfiguration du produit.

## <a name="remarks"></a>Notes

sur Windows 2000, le bouton **modifier** du produit est désactivé dans **ajout/suppression de programmes** du **panneau de configuration**.

Cette propriété peut être définie par une transformation de personnalisation pour empêcher les utilisateurs de modifier la personnalisation d’un administrateur via **Ajout/suppression de programmes**. Cette propriété affecte uniquement **Ajout/suppression de programmes**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Exemple de transformation de personnalisation](a-customization-transform-example.md)
</dt> </dl>

 

 




