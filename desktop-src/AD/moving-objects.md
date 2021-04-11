---
title: Déplacement d’objets
description: Déplacement d’objets
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Exemples de Active Directory Active Directory, déplacement d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030997"
---
# <a name="moving-objects"></a>Déplacement d’objets

Pour déplacer un objet au sein d’un domaine, utilisez la méthode [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

**Pour déplacer un objet dans un domaine**

1.  Crée une liaison avec l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) de l’objet à déplacer.
2.  Obtient l’ADsPath de l’objet à déplacer à partir de la propriété [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .
3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) du conteneur dans lequel l’objet sera déplacé.
4.  Déplacez l’objet avec la méthode [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .

S’il existe une interface pour l’objet qui a été déplacé, l’interface n’est pas valide après le déplacement de l’objet, car l’objet d’annuaire représenté par l’interface n’existe plus.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment déplacer un objet, consultez l' [exemple de code pour déplacer un objet](example-code-for-moving-an-object.md).

 

 