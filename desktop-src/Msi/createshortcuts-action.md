---
description: L’action CreateShortcuts gère la création de raccourcis.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Action CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091906"
---
# <a name="createshortcuts-action"></a>Action CreateShortcuts

L’action CreateShortcuts gère la création de raccourcis.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action CreateShortcuts doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [RemoveShortcuts](removeshortcuts-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | Identificateur du raccourci créé. |



 

## <a name="remarks"></a>Notes

L’action CreateShortcuts crée des raccourcis vers les fichiers de clé des composants des fonctionnalités qui sont sélectionnés pour l’installation ou la publication.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tableau de raccourcis](shortcut-table.md)
</dt> <dt>

[Table MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 



