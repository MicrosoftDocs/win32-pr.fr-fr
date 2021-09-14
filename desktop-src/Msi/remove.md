---
description: La valeur de la propriété supprimer est une liste de fonctionnalités délimitée par des virgules qui doivent être supprimées.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE (propriété)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218721"
---
# <a name="remove-property"></a>REMOVE (propriété)

La valeur de la propriété **supprimer** est une liste de fonctionnalités délimitée par des virgules qui doivent être supprimées. Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature](feature-table.md). Notez que si vous utilisez REMOVE = ALL sur la ligne de commande, le programme d’installation supprime toutes les fonctionnalités dont le niveau d’installation est supérieur à 0. Dans ce cas, le programme d’installation ne supprime pas les fonctionnalités dont le niveau d’installation est égal à 0. Pour plus d’informations sur le niveau d’installation des fonctionnalités, consultez [table](feature-table.md)des fonctionnalités.

## <a name="remarks"></a>Notes

Pour déterminer si un produit a été configuré pour être complètement désinstallé, l’auteur d’un package peut utiliser une expression conditionnelle pour vérifier si REMOVE = ALL. Notez que si le produit est supprimé en affectant à sa fonctionnalité supérieure la valeur absent, la propriété **supprimer** ne peut pas être égale à tout jusqu’à la fin de l' [action InstallValidate](installvalidate-action.md). Cela signifie que toute action personnalisée qui dépend de REMOVE = ALL doit être séquencée après InstallValidate. Pour plus d’informations, consultez également les [actions de conditionnement à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md). Notez que les noms de fonctionnalités respectent la casse.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :

1.  [**ADDLOCAL**](addlocal.md)
2.  **Installez**
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**INSTALLÉ**](reinstall.md)
6.  [**PUBLIÉS**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Par exemple, si la ligne de commande spécifie ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source. Si la ligne de commande est ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, alors que ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




