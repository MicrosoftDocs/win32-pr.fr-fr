---
title: Propriété DefaultCommand
description: Propriété DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031165"
---
# <a name="defaultcommand-property"></a>Propriété DefaultCommand

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la commande par défaut de l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

Caractères agent. ** ** *  * **(«***CharacterID***»). Chaîne Commands. DefaultCommand** \[  =  \]



| Partie     | Description                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Valeur de chaîne identifiant le nom (ID) de la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété vous permet de définir une [**commande**](/windows/desktop/lwef/the-command-object) dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) comme commande par défaut, en la rendant en gras. Cela ne modifie pas réellement les événements de gestion des commandes ou de double-clic.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 