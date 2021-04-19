---
description: Dans certains cas, un utilisateur qui n’est pas un administrateur système ne peut pas remplacer une liste approuvée de propriétés publiques Windows Installer limitées.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propriétés publiques restreintes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530889"
---
# <a name="restricted-public-properties"></a>Propriétés publiques restreintes

Dans le cas d’une installation gérée, l’auteur du package peut avoir besoin de limiter les [propriétés publiques](public-properties.md) qui sont transmises côté serveur et peut être modifiée par un utilisateur qui n’est pas un administrateur système. Certaines restrictions sont généralement nécessaires pour maintenir un environnement sécurisé lorsque l’installation requiert que le programme d’installation utilise des privilèges élevés. Si toutes les conditions suivantes sont réunies, un utilisateur qui n’est pas un administrateur système peut uniquement remplacer une liste approuvée de propriétés publiques restreintes :

-   Le système est Windows 2000.
-   L’utilisateur n’est pas un administrateur système.
-   L’application ou le produit est en cours d’installation avec des privilèges élevés.

Si toutes les conditions ci-dessus sont vraies, le programme d’installation se trouve par défaut dans la liste suivante de propriétés publiques restreintes qui peuvent être modifiées par n’importe quel utilisateur :

-   [**TRANSACTIONNEL**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NOCOMPANYNAME**](nocompanyname.md)
-   [**NOM de l’utilisateur**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**CORRECTIF**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**INITIAL**](reboot.md)
-   [**INSTALLÉ**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**RESUME**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**TRANSFORMATIONS**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

L’auteur d’un package d’installation peut étendre cette liste par défaut pour inclure des propriétés publiques supplémentaires à l’aide de la propriété [**SecureCustomProperties**](securecustomproperties.md) .

La définition de la propriété [**EnableUserControl**](-enableusercontrol.md) ou de la [stratégie système](system-policy.md) [EnableUserControl](enableusercontrol.md)étend la liste à toutes les propriétés publiques. Tous les utilisateurs peuvent ensuite modifier toute propriété publique.

Le programme d’installation définit la propriété [**RestrictedUserControl**](restrictedusercontrol.md) chaque fois que la liste des propriétés publiques transmises au serveur par des utilisateurs non-administrateurs est limitée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> </dl>

 

 



