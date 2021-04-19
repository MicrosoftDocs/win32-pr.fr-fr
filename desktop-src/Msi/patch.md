---
description: Le programme d’installation définit la propriété PATCH sur une liste de correctifs appliqués en appelant MsiApplyPatch, MsiApplyMultiplePatches ou l’option de ligne de commande/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Propriété PATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530340"
---
# <a name="patch-property"></a>Propriété PATCH

Le programme d’installation définit la propriété **patch** sur une liste de correctifs appliqués en appelant [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) ou l’option de [ligne de commande](command-line-options.md)/p. Vous pouvez également définir la propriété **patch** sur la ligne de commande lors de l’installation d’un package à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou de l’option de ligne de commande/i.

La valeur de la propriété **patch** est la liste des correctifs en cours d’installation. Chaque correctif de la liste est représenté par le chemin d’accès complet au package du correctif (fichier. msp). Les chemins d’accès complets de la liste sont séparés par des points-virgules.

**Windows Installer 2,0 :** Plusieurs correctifs ne sont pas pris en charge. Windows Installer 3,0 est requis pour appliquer plusieurs correctifs.

## <a name="remarks"></a>Notes

Si vous créez un package de correctifs à l’aide de [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) vous pouvez spécifier qu’une action ou une boîte de dialogue s’exécute uniquement lorsqu’un correctif particulier est appliqué. Lorsque vous créez le package de correctifs, par exemple test. msp, vous créez une image mise à niveau du produit et un fichier de propriétés de création de correctifs. Lors de la création du fichier de propriétés de création de correctifs, vous pouvez entrer un nom de propriété, par exemple PATCHFORTEST, dans le champ MediaSrcPropName de la table [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) . Lorsque vous créez les tables de séquence de l’image mise à niveau du produit, vous pouvez inclure dans la colonne condition de la table de séquence une instruction conditionnelle pour l’action ou la boîte de dialogue que vous souhaitez rendre conditionnelle.

Par exemple, vous pouvez utiliser l’instruction conditionnelle suivante pour exécuter une action ou une boîte de dialogue uniquement lorsque test. msp est appliqué.

<dl> PATCH ET PATCHFORTEST ET PATCH >< PATCHFORTEST  
</dl>

> [!Note]  
> Étant donné que la propriété **patch** peut contenir plusieurs correctifs, utilisez l’opérateur de sous-chaîne « >< » pour tester la présence d’un correctif spécifique plutôt que l’opérateur égal « = ». Pour plus d’informations sur les instructions conditionnelles, consultez la section [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md) .

 

Le programme d’installation définit les deux propriétés si vous appliquez une liste de correctifs incluant test. msp. Par exemple, vous pouvez utiliser l' [option de ligne de commande](command-line-options.md) /p pour appliquer une liste de deux correctifs.

**msiexec/qb/p \\ \\ éraflure \\ Scratch \\ \\ \\ test. msp ; \\ \\ éraflures \\ \\ xyz \\ bar. msp**

Le programme d’installation définit les propriétés **patch** et PATCHFORTEST comme suit.

<dl> PATCH = éraflure \\ \\ \\ Scratch \\ \\ \\ test. msp \\ \\ éraflures \\ \\ xyz \\ bar. msp  
PATCHFORTEST = éraflure \\ \\ \\ Scratch \\ \\ \\ test. msp  
</dl>

Dans ce cas, la condition est TRUE et la boîte de dialogue ou l’action conditionnelle ci-dessus peut s’exécuter pour chaque correctif installé, test. msp et bar. msp.

Si test. msp n’est pas appliqué, le programme d’installation ne l’inclut pas dans la propriété **patch** et ne définit pas PATCHFORTEST. Dans ce cas, la condition ci-dessus a la valeur FALSe et la boîte de dialogue ou l’action conditionnelle ne s’exécute pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
</dt> <dt>

[Exemples de syntaxe d’instruction conditionnelle](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




