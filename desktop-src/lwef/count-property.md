---
title: Count, propriété
description: Count, propriété
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842166"
---
# <a name="count-property"></a>Count, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne un entier long (propriété en lecture seule) qui spécifie le nombre d’objets [**Command**](/windows/desktop/lwef/the-command-object) dans la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). Commands. Count**

</dd> </dl>

## <a name="remarks"></a>Notes

**Count** comprend uniquement le nombre d’objets de [**commande**](/windows/desktop/lwef/the-command-object) que vous définissez dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Le serveur ou d’autres entrées du client ne sont pas inclus.

 

 