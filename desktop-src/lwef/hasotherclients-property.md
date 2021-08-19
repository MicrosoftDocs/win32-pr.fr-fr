---
title: Propriété HasOtherClients
description: Propriété HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479004"
---
# <a name="hasotherclients-property"></a>Propriété HasOtherClients

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur indiquant si le caractère spécifié est utilisé par d’autres applications.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent*. **Caractères («**_CharacterID_*_»). HasOtherClients_*



| Valeur     | Description                                |
|-----------|--------------------------------------------|
| **True**  | Le caractère comporte d’autres clients.           |
| **False** | Le caractère n’a pas d’autres clients. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette propriété pour déterminer si votre application est le seul ou dernier client du caractère, lorsque plusieurs applications partagent le même caractère (a chargé).

 

 




