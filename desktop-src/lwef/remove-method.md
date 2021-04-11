---
title: Remove (méthode)
description: Remove (méthode)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315137"
---
# <a name="remove-method"></a>Remove (méthode)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Supprime un objet [**Command**](/windows/desktop/lwef/the-command-object) de la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID ***»). Commands. Remove*** Name*



| Partie   | Description                                                       |
|--------|-------------------------------------------------------------------|
| *Nom* | Obligatoire. Valeur de chaîne correspondant à l’ID de la commande. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsqu’un objet [**Command**](/windows/desktop/lwef/the-command-object) est supprimé de la collection, il n’apparaît plus lorsque le menu contextuel du caractère s’affiche ou dans la fenêtre commandes lorsque votre application cliente est en entrée active.

## <a name="see-also"></a>Voir aussi

[**RemoveAll, méthode**](removeall-method.md)


 

 