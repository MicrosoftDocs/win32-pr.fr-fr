---
description: L’action RemoveIniValues supprime .ini informations de fichier spécifiées pour la suppression dans la table RemoveIniFile si le composant est configuré pour être installé localement ou exécuté à partir de la source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Action RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626388"
---
# <a name="removeinivalues-action"></a>Action RemoveIniValues

L’action RemoveIniValues supprime .ini informations de fichier spécifiées pour la suppression dans la [table RemoveIniFile](removeinifile-table.md) si le composant est configuré pour être installé localement ou exécuté à partir de la source. L’action RemoveIniValues supprime .ini informations de fichier qui ont été associées à un composant dans la [table inifile](inifile-table.md). Cette action supprime également les informations de .ini fichier si les informations ont été écrites par l' [action WriteIniValues](writeinivalues-action.md) et que le composant est programmé pour être désinstallé.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit être appelée avant l’action RemoveIniValues. Si une action [WriteIniValues](writeinivalues-action.md) est utilisée dans la séquence, elle doit apparaître après RemoveIniValues.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action    |
|-------|-------------------------------|
| \[1\] | Identificateur du fichier .ini.      |
| \[2\] | Section clé de fichier .ini.     |
| \[3\] | Élément supprimé du fichier .ini.  |
| \[4\] | Valeur supprimée du fichier .ini. |



 

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

 

 



