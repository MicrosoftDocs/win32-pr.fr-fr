---
description: L’objet Address représente une entité qui peut émettre ou recevoir des appels.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objet Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866614"
---
# <a name="address-object"></a>Objet Address

L’objet Address représente une entité qui peut émettre ou recevoir des appels. Cet objet expose des interfaces et des méthodes qui permettent à une application d’effectuer un certain nombre d’opérations, telles que :

-   Détecte si une adresse spécifiée peut prendre en charge un ensemble particulier de besoins de type de média.
-   Énumérer les appels actuellement associés à l’adresse.
-   Créer ou transférer des appels.
-   Obtient le nom du fournisseur de services associé.
-   Si un fournisseur de services multimédia existe, récupérez les pointeurs d’interface qui autorisent la manipulation détaillée des terminaux.
-   Récupérez et définissez d’autres informations, par exemple si un message est en attente.

La plupart des adresses sont associées à un terminal, mais cela n’est pas uniformément le cas. Par exemple, un TSP distant qui fournit l’accès à l’équipement sur un serveur aura une adresse sur l’ordinateur local, mais pas sur un terminal. Un modem sans conférencier n’a pas non plus de terminal associé à son adresse.

Si une adresse n’est pas associée à un terminal, l’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) n’est pas exposée sur l’objet.

L’exemple de code de [sélection d’adresse](select-an-address.md) illustre le processus de base pour l’acquisition d’un pointeur d’objet d’adresse.

Pour obtenir la liste de toutes les interfaces associées à l’objet Address, consultez [interfaces d’objet Address](address-object-interfaces.md) .

 

 
