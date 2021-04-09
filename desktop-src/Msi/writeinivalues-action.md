---
description: L’action WriteIniValues écrit les informations du fichier. ini que l’application a besoin d’écrire dans ses fichiers. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Action WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866049"
---
# <a name="writeinivalues-action"></a>Action WriteIniValues

L’action WriteIniValues écrit les informations du fichier. ini que l’application a besoin d’écrire dans ses fichiers. ini. L’écriture de ces informations est contrôlée par la [table des composants](component-table.md). Une valeur. ini est écrite si le composant correspondant a été configuré pour être installé localement ou exécuté à partir de la source.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallValidate doit précéder l’action WriteIniValues. S’il existe une [action RemoveIniValues](removeinivalues-action.md) dans la séquence, elle doit être antérieure à l’action WriteIniValues.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action              |
|-------|-----------------------------------------|
| \[1\] | Identificateur du fichier. ini.                |
| \[2\] | clé du fichier. ini dans la section suivante. |
| \[3\] | Élément supprimé du fichier. ini.            |
| \[4\] | Valeur supprimée du fichier. ini.           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table IniFile](inifile-table.md)
</dt> </dl>

 

 



