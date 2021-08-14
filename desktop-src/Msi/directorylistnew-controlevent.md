---
description: Cet événement avertit le contrôle DirectoryList qu’un nouveau dossier doit être créé ; Il crée le nouveau dossier et sélectionne le champ nom du dossier pour le modifier.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378899"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent,

Cet événement avertit le [contrôle DirectoryList](directorylist-control.md) qu’un nouveau dossier doit être créé ; Il crée le nouveau dossier et sélectionne le champ nom du dossier pour le modifier. Le nom par défaut du nouveau dossier peut être créé dans la [table UIText](uitext-table.md). Entrez « NewFolder » dans la colonne clé. Entrez la valeur du nom par défaut du nouveau dossier dans la colonne de texte. Cette valeur doit se présenter sous la forme d’un type de données de colonne de [nom de fichier](filename.md) et utiliser la \| syntaxe SFN LFN. Si cette valeur n’est pas présente dans la table UIText ou n’est pas une valeur valide, le programme d’installation utilise la valeur par défaut « FLDR \| New Folder ». Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).

Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement. L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Notez que si ce ControlEvent, est rappelé lorsqu’un nouveau dossier existe déjà, un deuxième dossier ne sera pas créé. Dans ce cas, l’appel de DirectoryListNew sélectionne le nom du nouveau dossier existant pour la modification.

## <a name="published-by"></a>Publié par

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher la création d’un nouveau dossier.

 

 



