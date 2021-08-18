---
title: Propriété DefaultCommand
description: Propriété DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693634"
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

Caractères agent. ** ** *  * **(«**_CharacterID_*_»). Chaîne Commands. DefaultCommand_* \[  =  \]



| Partie     | Description                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Valeur de chaîne identifiant le nom (ID) de la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette propriété vous permet de définir une [**commande**](/windows/desktop/lwef/the-command-object) dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) comme commande par défaut, en la rendant en gras. Cela ne modifie pas réellement les événements de gestion des commandes ou de double-clic.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 