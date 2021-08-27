---
description: La fonction SetupSetSourceList ouvre ou crée une liste source sur le système de l’utilisateur.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Utilisation de la liste de sources MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100629"
---
# <a name="using-the-mru-source-list"></a>Utilisation de la liste de sources MRU

La fonction [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) ouvre ou crée une liste source sur le système de l’utilisateur. Vous pouvez choisir de définir la liste des utilisateurs, la liste système, une combinaison des listes utilisateur et système ou une liste temporaire comme liste de sources MRU. Si une liste temporaire est utilisée, il s’agit de la seule liste disponible pour l’application d’installation jusqu’à ce que [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) soit appelé, ou **SetupSetSourceList** est appelée une deuxième fois.

Une fois qu’une liste est définie, vous pouvez interroger la liste source à l’aide de [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) pour obtenir un tableau des chemins d’accès source. Lorsque le tableau de liste source n’est plus nécessaire, vous devez appeler la fonction [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) pour libérer les ressources allouées par [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Pour ajouter un chemin d’accès à une liste source, l’un d’eux résidant sur le système de l’utilisateur ou une liste temporaire, appelez [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Si la liste source spécifiée n’est pas temporaire, cette source restera sur le système de l’utilisateur et sera accessible aux installations suivantes.

Pour supprimer un chemin d’accès du chemin source, appelez la fonction [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .

 

 



