---
title: Remove (méthode)
description: Remove (méthode)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3337fb25db49f1d6c8ccd6d94f2817340db226e14718cfa7943940fbfb069b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882780"
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

*agent ***. Caractères («**_CharacterID_*_»). Commands. Remove_ * _Name_



| Partie   | Description                                                       |
|--------|-------------------------------------------------------------------|
| *Nom* | Obligatoire. Valeur de chaîne correspondant à l’ID de la commande. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsqu’un objet [**Command**](/windows/desktop/lwef/the-command-object) est supprimé de la collection, il n’apparaît plus lorsque le menu contextuel du caractère s’affiche ou dans la fenêtre commandes lorsque votre application cliente est en entrée active.

## <a name="see-also"></a>Voir aussi

[**RemoveAll, méthode**](removeall-method.md)


 

 