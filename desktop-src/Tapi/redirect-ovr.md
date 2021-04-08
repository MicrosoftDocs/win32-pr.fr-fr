---
description: La redirection de session permet à une application de dévier une session proposée vers une autre adresse sans répondre à l’appel.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Rediriger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760809"
---
# <a name="redirect"></a>Rediriger

La redirection de session permet à une application de dévier une session proposée vers une autre adresse sans répondre à l’appel. L’application peut effectuer une redirection appel par appel. Par exemple, une application peut permettre à un utilisateur de spécifier des redirections différentes en fonction des informations sur l’ID de l’appelant. Une fois qu’un appel a été redirigé avec succès, l’état passe généralement à inactif et les ressources associées doivent être libérées.

La redirection diffère [par rapport à](forward-ovr.md) ce qu’une fois que le transfert a été configuré, l’opération est effectuée par l’interface TAPI, le fournisseur de services ou le commutateur sans intervention supplémentaire de l’application. La redirection diffère du [transfert](transfer-ovr.md) dans le fait que la redirection ne nécessite pas de réponse préalable à l’appel.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
