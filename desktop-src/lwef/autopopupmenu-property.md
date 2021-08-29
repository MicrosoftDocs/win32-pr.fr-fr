---
title: Propriété AutoPopupMenu
description: Propriété AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29659fac026323ec5b2db4794443ff680df9d378c43ecfec415e78c9d4ce7e5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114839"
---
# <a name="autopopupmenu-property"></a>Propriété AutoPopupMenu

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si le fait de cliquer avec le bouton droit sur le caractère ou l’icône de la barre des tâches affiche automatiquement le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***caractères * * * * ("**_CharacterID_*_"). AutoPopupMenu_ *  \[  =  *booléen*\]



| Partie      | Description                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si le serveur affiche automatiquement le menu contextuel du caractère en cliquant dessus avec le bouton droit. **True** (par défaut) affiche le menu en cliquant avec le bouton droit. <br/> **Valeur false** N’affiche pas le menu en cliquant avec le bouton droit.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

En affectant à cette propriété la **valeur false**, vous pouvez créer votre propre comportement de gestion de menus. Pour afficher le menu après avoir défini cette propriété sur **false**, utilisez la méthode [**ShowPopupMenu**](showpopupmenu-method.md) .

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**Méthode ShowPopupMenu**](showpopupmenu-method.md)


 

 





