---
description: L’action RemoveIniValues supprime les informations de fichier. ini spécifiées pour la suppression dans la table RemoveIniFile si le composant est configuré pour être installé localement ou exécuté à partir de la source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Action RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953005"
---
# <a name="removeinivalues-action"></a>Action RemoveIniValues

L’action RemoveIniValues supprime les informations de fichier. ini spécifiées pour la suppression dans la [table RemoveIniFile](removeinifile-table.md) si le composant est configuré pour être installé localement ou exécuté à partir de la source. L’action RemoveIniValues supprime les informations du fichier. ini qui ont été associées à un composant dans la [table inifile](inifile-table.md). Cette action supprime également les informations du fichier. ini si les informations ont été écrites par l' [action WriteIniValues](writeinivalues-action.md) et que la désinstallation du composant est planifiée.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit être appelée avant l’action RemoveIniValues. Si une action [WriteIniValues](writeinivalues-action.md) est utilisée dans la séquence, elle doit apparaître après RemoveIniValues.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action    |
|-------|-------------------------------|
| \[1\] | Identificateur du fichier. ini.      |
| \[2\] | Section clé du fichier. ini.     |
| \[3\] | Élément supprimé du fichier. ini.  |
| \[4\] | Valeur supprimée du fichier. ini. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table RemoveIniFile](removeinifile-table.md)
</dt> <dt>

[Table IniFile](inifile-table.md)
</dt> <dt>

[Action WriteIniValues](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 



