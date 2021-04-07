---
title: Propriété HasOtherClients
description: Propriété HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029240"
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

*agent*. **Caractères («***CharacterID***»). HasOtherClients**



| Valeur     | Description                                |
|-----------|--------------------------------------------|
| **True**  | Le caractère comporte d’autres clients.           |
| **False** | Le caractère n’a pas d’autres clients. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser cette propriété pour déterminer si votre application est le seul ou dernier client du caractère, lorsque plusieurs applications partagent le même caractère (a chargé).

 

 




