---
description: Dans l’exemple suivant, un socket multipoint est souvent caractérisé par la description de son rôle dans l’un des deux plans (contrôle ou données).
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: Sémantique SPI pour joindre des feuilles multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530579"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>Sémantique SPI pour joindre des feuilles multipoint

Dans l’exemple suivant, un socket multipoint est souvent caractérisé par la description de son rôle dans l’un des deux plans (contrôle ou données). Il est important de comprendre que ce même socket a un rôle dans l’autre plan, mais cela n’est pas mentionné afin de conserver les références courtes. Par exemple, une référence à un \_ Socket racine c peut faire référence à une racine racine \_ /d ou à un \_ \_ Socket feuille c racine/d \_ .

Dans les schémas de plan de contrôle enracinés, de nouveaux nœuds terminaux sont ajoutés à une session multipoint dans l’une ou l’autre des deux méthodes. Dans la première méthode, la racine utilise [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour établir une connexion avec un nœud terminal et l’inviter à devenir participant. Sur le nœud terminal, l’application homologue doit avoir créé un \_ Socket feuille c et utilisé [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) pour le définir en mode écoute. Le nœud terminal reçoit une indication FD \_ Accept lorsqu’il est invité à rejoindre la session, et signale sa volonté de s’y joindre en appelant [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). L’application racine reçoit une indication FD \_ Connect lorsque l’opération de jointure est terminée.

Dans la deuxième méthode, les rôles sont fondamentalement inversés. Le client racine crée un \_ Socket racine c et le définit en mode écoute. Un nœud feuille souhaitant rejoindre la session crée un \_ Socket feuille c et utilise [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) pour initier la connexion et demander des admission. Le client racine reçoit le FD \_ Accept lorsqu’une demande admission entrante arrive et admet le nœud terminal en appelant [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). Le nœud terminal reçoit FD \_ Connect lorsqu’il a été admis.

Dans un plan de contrôle sans racine, où tous les nœuds sont des \_ feuilles c, la fonction [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) est utilisée pour initialiser l’inclusion d’un nœud dans une session multipoint existante. Une \_ indication FD Connect est fournie lorsque la jointure est terminée et que le descripteur de socket retourné est utilisable dans la session multipoint. Dans le cas de la multidiffusion IP, cela correspond à l' \_ option IP ajouter \_ un socket d’appartenance.

Il existe, par conséquent, trois instances où un client utilise [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf):

-   Agir comme racine multipoint et inviter une nouvelle feuille pour rejoindre la session.
-   Action en tant que feuille effectuant une demande admission à une session multipoint avec racine.
-   Agissant comme une feuille de recherche de admission dans une session multipoint sans racine (par exemple, la multidiffusion IP).

 

 
