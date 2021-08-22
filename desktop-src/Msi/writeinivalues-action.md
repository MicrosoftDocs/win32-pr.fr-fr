---
description: L’action WriteIniValues écrit les informations de fichier .ini que l’application a besoin d’écrire dans ses fichiers .ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Action WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942097"
---
# <a name="writeinivalues-action"></a>Action WriteIniValues

L’action WriteIniValues écrit les informations de fichier .ini que l’application a besoin d’écrire dans ses fichiers .ini. L’écriture de ces informations est contrôlée par la [table des composants](component-table.md). Une valeur .ini est écrite si le composant correspondant a été configuré pour être installé localement ou exécuté à partir de la source.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallValidate doit précéder l’action WriteIniValues. S’il existe une [action RemoveIniValues](removeinivalues-action.md) dans la séquence, elle doit être antérieure à l’action WriteIniValues.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action              |
|-------|-----------------------------------------|
| \[1\] | Identificateur du fichier .ini.                |
| \[2\] | .ini clé de fichier dans la section suivante. |
| \[3\] | Élément supprimé du fichier .ini.            |
| \[4\] | Valeur supprimée du fichier .ini.           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table IniFile](inifile-table.md)
</dt> </dl>

 

 



